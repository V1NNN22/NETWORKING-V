# ☁️ Why Cloud Routing Tables Are Static and Don’t Use OSPF/BGP Internally  
## Written By: Vinod N. Rathod  

---

## 🌥️ The Core Question

Why do cloud VPCs use static route tables instead of dynamic routing protocols like OSPF, BGP, or EIGRP inside the VPC?

**Short Answer:**  
Because cloud routing is software-defined, centrally controlled, multi-tenant, and massively scalable—while dynamic routing depends on neighbor discovery, L2 adjacency, and routing state exchange, all of which are incompatible with cloud architecture.

---

## 🧩 1. How Routing Works On-Prem

Traditional routing protocols:

- **OSPF**
- **BGP**
- **EIGRP**
- **IS-IS**

They rely on:

- LSA flooding  
- neighbor adjacency  
- routing updates  
- multicast/broadcast packets  
- shared topology visibility  

These mechanisms depend entirely on **Layer 2 connectivity** and predictable router neighbors.

Cloud VPCs intentionally avoid all of this.

---

## ☁️ 2. Cloud Routing = Static Route Tables + SDN

Cloud routing exposes only:
No:

- adjacency  
- dynamic route exchange  
- routing protocol daemon  
- link-state learning  

Routing decisions are made by:

- SDN controllers  
- hypervisors  
- provider-managed underlay routers  
- internal proprietary routing systems  

Customer-visible routing remains **simple and static**.

---

## 🔐 3. Reason 1: Multi-Tenant Isolation

Dynamic routing protocols require:

- multicast  
- hello packets  
- neighbor discovery  

If AWS allowed OSPF/BGP inside VPCs:

- tenants could inject rogue routes  
- VPC-to-VPC route leaks would occur  
- malicious LSAs could poison the network  
- shared routers could be attacked  
- underlay security would collapse  

Static routing ensures **perfect isolation**.

---

## ⚙️ 4. Reason 2: Hyperscale Makes Dynamic Routing Impossible

Cloud scale = enormous:

- millions of VPCs  
- billions of ENIs  
- thousands of routing nodes  
- workloads scaling up/down every minute  

Dynamic routing would cause:

- nonstop route churn  
- massive LSA floods  
- meltdown of control-plane  
- catastrophic convergence times  

Static routing = stable, deterministic, scalable.

---

## 📡 5. Reason 3: Underlay Routing Is Proprietary & Hidden

Cloud providers use:

- custom traffic engineering  
- private link-state protocols  
- ECMP everywhere  
- fast rerouting  
- optimized spine-leaf fabrics  

They cannot expose:

- underlay topology  
- internal route advertisements  
- backbone routing logic  

Static user routing avoids conflict with these hidden systems.

---

## 🛰️ 6. Reason 4: No Layer 2 = No Dynamic Routing

OSPF requires multicast:

- 224.0.0.5
- 224.0.0.6

EIGRP requires multicast:

- 224.0.0.10

BGP requires adjacency and reachable neighbors.

Cloud VPCs have:

- **no broadcast**
- **no multicast**
- **no L2 adjacency**
- **no ARP flooding**

Therefore dynamic routing literally **cannot function** inside a VPC.

---

## 🧱 7. Reason 5: Static Routing Works Perfectly With Cloud APIs

Cloud networking is:

- policy-based  
- programmable  
- auditable  
- API-driven  
- automated via IaC  

Dynamic routing:

- reacts automatically to changes  
- can introduce instability  
- breaks intent-based networking  

Static routing:

- predictable  
- fully automated  
- aligns with IaC workflows  
- easy to audit  

Cloud prefers **deterministic policy**, not dynamic negotiation.

---

## 🌐 8. Where Dynamic Routing *Is* Allowed

Only at **cloud edges**, never inside VPCs.

Allowed with BGP:

- **VPN tunnels**
- **Direct Connect**
- **ExpressRoute**
- **Partner Interconnect**

Not allowed:

- routing between EC2 instances  
- OSPF/BGP inside VPC  
- dynamic routing for VPC peering  
- advertisement from subnets  

Dynamic routing is strictly limited to **hybrid connectivity**.

---

## 🔍 9. Example: Why EC2 Cannot Advertise Routes

If an EC2 instance runs BGP:

- VPC router will NOT peer  
- no adjacency forms  
- no inbound routing updates  
- no support for neighbor discovery  
- packets are dropped  

Only the route table or TGW can accept routing entries—via static updates or APIs.

---

## 🚀 10. Summary Table

| Aspect | Traditional Routing | Cloud VPC Routing | Reason |
|--------|----------------------|-------------------|--------|
| Routing Model | Dynamic | Static | Multi-tenancy + safety |
| Protocols | OSPF, BGP | None | No L2/multicast |
| Adjacencies | Required | Blocked | Isolation & security |
| Scaling | Limited | Massive | SDN control |
| Visibility | Hop-level | Abstracted | Simplification |
| Changes | Automatic | API-driven | Deterministic |
| Underlay | Customer-controlled | Provider-controlled | Hidden |

---

## 🧠 In Simple Terms

> Cloud VPCs use static routing because dynamic routing cannot coexist with multi-tenancy, hyperscale, or the lack of Layer 2 in cloud networks.

Static routing + SDN gives cloud providers the necessary **control, security, predictability, and scalability**.
---
## ~ V1NNN22 ~
## THANKYOU! 