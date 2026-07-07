# MPLS Label Stack in Networking
~
## Written By: VINOD N. RATHOD.
~

## What is MPLS Label Stack?
- **Definition:** A technique where multiple MPLS labels are attached to a packet, allowing routers to perform different forwarding tasks at different network layers.
- **Purpose:** Enables advanced routing features like VPNs, Traffic Engineering (TE), and Segment Routing.
- **Analogy:** Like placing multiple shipping labels on a parcel. Each warehouse removes its own label until the package reaches the final destination.

---

## The 4 Core Steps of MPLS Label Stack Operation

### 1. Label Push (Step 1)
- **Function:** One or more labels are added to the packet.
- **Role:** Identifies the forwarding path and network service.
- **Examples:** Outer label for MPLS path, inner label for VPN.

---

### 2. Label Switching (Step 2)
- **Function:** Intermediate Label Switch Routers (LSRs) swap only the top label.
- **Role:** Forward packets without checking the IP header.
- **Examples:** Top label changes at every MPLS hop.

---

### 3. Label Pop (Step 3)
- **Function:** The top label is removed when its job is complete.
- **Role:** Reveals the next label underneath.
- **Examples:** Outer transport label removed before entering the VPN network.

---

### 4. Final Delivery (Step 4)
- **Function:** Remaining label or IP packet reaches its destination.
- **Role:** Delivers traffic to the correct customer or network.
- **Examples:** VPN label directs the packet to the correct customer site.

---

## Key Features
- **Multiple Labels:** Supports layered forwarding.
- **Fast Switching:** Routers process labels instead of IP lookups.
- **Traffic Engineering:** Optimizes network paths.
- **VPN Support:** Enables MPLS Layer 3 and Layer 2 VPNs.

---

## Why It Matters
- **Scalability:** Supports large service provider networks.
- **Flexibility:** One packet can carry multiple forwarding instructions.
- **Performance:** Faster forwarding with reduced processing overhead.

---

## Quick Recap (Mnemonic)
- **Push → Switch → Pop → Deliver**
  - **Labels → LSR → Remove → Destination**

---

# THANK YOU!
# ~ **V1NNN22**