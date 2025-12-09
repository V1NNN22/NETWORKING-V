# ☁️ Why Cloud Load Balancers Don’t Always Preserve Source IP (And Why NAT Is Mandatory in Many Cases)  
## Written By: Vinod N. Rathod  

---

## 🌥️ The Core Question  

Why do cloud load balancers (ALB/NLB in AWS, Azure LB, GCP LB) sometimes **not preserve the client’s source IP**, and why must they perform **NAT** in many scenarios?  
Why can’t they behave like traditional on-prem load balancers where preserving source IP is easy?

**Short Answer:**  
Because cloud LBs are distributed, multi-AZ, multi-node, SDN-driven systems. They must use NAT to ensure symmetric routing, stable flows, multi-AZ consistency, backend isolation, and massive hyperscale performance. Traditional L2/L3 assumptions simply don’t exist in the cloud.

---

## 🧩 1. On-Prem Load Balancers Are Simple, Local Appliances  

A typical on-prem LB:

- sits in one location  
- has predictable L2/L3 topology  
- handles all flows centrally  
- can preserve source IP because return path is guaranteed  
- relies on ARP and MAC-based adjacency  

Preserving source IP works easily because everything is **physically local and Layer 2 adjacent**.

Cloud has none of this simplicity.

---

## ☁️ 2. Cloud Load Balancers Are Distributed Across Many Nodes  

Cloud LBs are:

- multi-AZ  
- running on many nodes  
- highly elastic  
- independent of any physical NIC  
- reachable via Anycast or edge paths  

Your “one” load balancer is actually:

> A fleet of LB nodes scattered across the region working as one virtual device.

If source IP were preserved without NAT:

- responses could go to the wrong node  
- flows would break  
- asymmetric routing would be unavoidable  

NAT solves this.

---

## 🔐 3. Reason 1: NAT Guarantees Symmetric Routing  

Scenario without NAT:

1. Request enters via LB node in AZ-A  
2. Backend is in AZ-B  
3. Response may exit via LB node in AZ-C  

Result:

- asymmetric routing  
- dropped packets  
- connection resets  
- unpredictable behavior  

NAT enforces a rule:

> The node that receives the request also handles the response.

This stabilizes connection flow.

---

## ⚙️ 4. Reason 2: NAT Hides Backend IPs for Multi-Tenant Security  

If cloud preserved raw source IPs without NAT:

- backend private IPs could leak  
- tenants might fingerprint cloud infrastructure  
- malicious traffic could target specific nodes  
- isolation boundaries weaken  

NAT ensures:

- backend IPs remain invisible  
- internal topology stays private  
- every tenant operates in a clean security bubble  

Multi-tenancy requires NAT as a security boundary.

---

## 📡 5. Reason 3: Preserving Source IP Breaks AZ Isolation  

Without NAT, preserving client IP means:

- responses may hairpin across AZs  
- cross-AZ charges increase  
- latency spikes  
- routing rules are violated  

Cloud must enforce strict AZ isolation for:

- cost boundaries  
- fault domains  
- predictable routing  

NAT keeps traffic contained and consistent.

---

## 🧱 6. Reason 4: Distributed Load Balancers Need Stateless Flow Distribution  

Cloud LBs use:

- flow hashing  
- distributed lookup tables  
- traffic sharding  
- multi-node routing logic  

If source IP were preserved:

- hashing becomes unpredictable  
- balancing becomes uneven  
- LB nodes must track more state  
- horizontal scale collapses  

NAT normalizes flows so nodes can share the load fairly.

---

## 🛰️ 7. Reason 5: Cloud LB Features Depend on NAT  

NAT is required for:

- cross-zone load balancing  
- connection stickiness  
- health-based routing  
- internal load balancers  
- TLS termination  
- L7 inspection and WAF  
- multi-AZ failover  

Preserving source IP would disable or break many of these features.

---

## 🌐 8. When Cloud **Does** Preserve Source IP  

Source IP is preserved when:

- using NLB in “preserve client IP” mode  
- traffic is pure L4  
- routing tables allow direct return path  
- backend can reach LB nodes reliably  

Even then:

- fewer features are supported  
- careful architecture is required  
- asymmetric routing risks still exist  

Preserving source IP in cloud is the exception, not the rule.

---

## 🔍 9. Why ALBs Never Preserve Client Source IP  

ALB is **not** a passthrough device. It is a **proxy**.

It:

- terminates TCP  
- decrypts TLS  
- rewrites HTTP  
- performs host/path routing  
- applies WAF rules  
- re-establishes new backend connections  

Once ALB terminates the connection, the original source IP cannot survive at L4.

Instead, ALB adds headers:

- `X-Forwarded-For`  
- `X-Forwarded-Port`  
- `X-Forwarded-Proto`  

These preserve client identity at the **application layer**, not the network layer.

---

## 🚀 10. Summary Table

| Reason | Why NAT Is Required |
|--------|----------------------|
| Symmetric routing | Ensures request + response flow through same LB node |
| Multi-AZ distribution | LB nodes are everywhere, NAT keeps flows consistent |
| Security | Hides backend IPs and internal topology |
| Tenant isolation | Prevents cross-tenant leakage and spoofing |
| Scaling | Enables distributed, stateless LB nodes |
| ALB L7 behavior | Proxying destroys original packet details |
| Cross-AZ behavior | Prevents hairpin loops and routing failures |

---

## 🧠 In Simple Terms

> Cloud load balancers don’t preserve source IP because they’re **not single appliances**.  
> They are **distributed systems**, and NAT is the glue that keeps traffic stable, secure, and symmetric.

Without NAT, cloud load balancers would fall apart at scale.

---
## ~ V1NNN22 ~
## THANKYOU! 