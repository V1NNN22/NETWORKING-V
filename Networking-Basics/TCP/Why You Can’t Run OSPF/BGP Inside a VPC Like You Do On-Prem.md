# ☁️ Why You Can’t Run OSPF/BGP Inside a VPC Like You Do On-Prem  
## Written By: Vinod N. Rathod

---

## 🌥️ The Core Question

If VPCs are virtual networks, why can’t you run routing protocols like **OSPF or BGP** inside them the same way you do on physical routers?

**Short Answer:**  
Because VPCs are **software-defined overlays**, not physical routers — and cloud providers intentionally prevent dynamic routing to preserve **multi-tenancy, isolation, scalability, and security**.

---

# 🧩 1. The Design Philosophy Difference

## On-Prem Networking
- You own routers/switches.  
- You control routing protocols.  
- You establish adjacencies & exchange routes.  
- Full visibility into topology and route changes.

## Cloud Networking
- “Router” is a virtual router managed by the provider.  
- No adjacency capability.  
- Only static routes via route tables.  
- Underlay routing is hidden and provider-controlled.

**Why:**  
Dynamic neighbor discovery cannot exist in a multi-tenant cloud with millions of isolated networks.

---

# 🧭 2. Cloud VPC = Overlay Network (Not a Router)

A VPC has:
- **No routing daemon**  
- **No OSPF/BGP support**  
- **No neighbor discovery**  
- **No multicast or hello packets**  
- **No ability to advertise or learn routes**

VPC routing is:
- **Declarative** (you define desired paths)  
- **Static** (manually or via automation)  

Everything runs on **SDN** — not hardware.

---

# 🔍 3. Why Dynamic Routing Protocols Are Blocked

### 1. Multi-Tenant Isolation
OSPF/BGP require:
- Broadcasts  
- Multicast  
- Route advertisements  

This would risk:
- Route leaks  
- Tenant cross-contamination  
- Instability across shared infrastructure

### 2. Scale Limitations
Cloud = millions of customers × millions of prefixes  
Dynamic routing would collapse at global scale.

### 3. Security
Dynamic routing introduces:
- Spoofing  
- Rogue advertisements  
- Path hijacking  

Unacceptable in a shared public cloud.

### 4. Hidden Underlay
You cannot peer with a router you cannot see.

---

# 🛠️ 4. Cloud Routing Model vs Traditional Routing

## Traditional Routing
- Automatic via OSPF/BGP  
- Full topology visibility  
- Dynamic convergence  
- Hop-by-hop control

## Cloud Routing
- Static route tables only  
- No protocol-driven learning  
- Underlay routing is opaque  
- Provider handles convergence internally

**Why:**  
Cloud must stay predictable and isolated.

---

# 🌐 5. Where Dynamic Routing *Does* Exist in Cloud

Dynamic routing is allowed only at the **cloud edge**.

### ✔ Allowed:
- **BGP with Direct Connect** (AWS)  
- **BGP with ExpressRoute** (Azure)  
- **BGP with Cloud Interconnect** (GCP)  
- **BGP over Site-to-Site VPN** (AWS/Azure/GCP)

### ❌ Not Allowed:
- EC2 ↔ VPC routing  
- Subnet ↔ Subnet dynamic routing  
- VPC ↔ VPC routing  
- Inside VPCs or VNets  

Reason: Only edge routers support BGP; internal VPC routers do not run routing protocols.

---

# 🔐 6. Why Cloud Providers Choose Static Routing

| Problem With Dynamic Routing | Cloud Reasoning |
|------------------------------|-----------------|
| Too many route advertisements | Breaks global scale |
| Route poisoning | Security risk |
| Requires trusted neighbors | Multi-tenant conflict |
| Protocol overhead | Increases latency/cost |
| Customer misconfigs | Global outages risk |

Static routing = predictable, safe, scalable.

---

# 📡 7. How Cloud Achieves “Dynamic” Behavior Without OSPF/BGP

Inside the underlay, the cloud provider uses:
- Proprietary routing protocols  
- Traffic engineering systems  
- ECMP (Equal-Cost Multi-Path)  
- Real-time automated failover  

Users never see this — only the outcome:
- Low latency  
- Fast convergence  
- High redundancy

The **underlay is dynamic**,  
but the **overlay (your VPC) must stay static**.

---

# 🧱 8. Practical Impact for Architects

Because OSPF/BGP aren’t supported inside VPCs:

- Routing must be managed manually  
- Use automation (IaC) for route updates  
- CIDR design is extremely important  
- Large environments require modular design  
- Use Transit Gateway / VNet Peering for aggregation  
- Avoid overlapping IPs  

Static routing forces cleaner architecture.

---

# ⚙️ 9. Example Scenario

**Question:**  
Why can’t EC2 instance A advertise a new subnet to instance B using BGP?

**Answer:**  
Because EC2 → VPC Router communication is **flow-based**, not adjacency-based.  
The VPC router does **not participate** in OSPF/BGP, and does **not accept** route advertisements.

You must update route tables manually or via IaC.

---

# 🚀 10. Summary Table

| Aspect | On-Prem Routing | Cloud Routing |
|--------|------------------|----------------|
| Routing Model | Dynamic | Static |
| Protocols | OSPF/BGP | None inside VPC |
| Adjacencies | Allowed | Blocked |
| Control | Full | Partial |
| Underlay Visibility | Full | Hidden |
| Route Updates | Automatic | Manual/API |
| Multi-Tenancy | No | Yes |

---

# 🧠 In Simple Terms

> You can’t run OSPF/BGP inside a VPC because a VPC isn’t a real router — it’s an SDN abstraction.  
Dynamic routing would break **isolation, security, and cloud-scale architecture**.

Cloud routing must remain **static, controlled, and predictable**.

---
## ~ V1NNN22 ~
## THANKYOU! 