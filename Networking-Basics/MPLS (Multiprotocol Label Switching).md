# MPLS (Multiprotocol Label Switching)  
~
## Written By: VINOD N. RATHOD.  
~

## What is MPLS?  
- **Definition:** A data forwarding technique that uses labels instead of IP addresses to route packets efficiently across networks.  
- **Purpose:** Speeds up packet forwarding and enables traffic engineering → commonly used by ISPs.  
- **Analogy:** Like attaching a fast-pass tag on luggage so it skips detailed checking at every checkpoint.  

---

## The 4 Core Steps of MPLS Operation  

### 1. Label Assignment (Step 1)  
- **Function:** Ingress router assigns a label to incoming packet.  
- **Role:** Replaces complex IP lookup with simple label.  
- **Examples:** Label added at network entry point.  

---

### 2. Label Switching (Step 2)  
- **Function:** Intermediate routers forward packets based on labels.  
- **Role:** Uses Label Switching Tables instead of routing tables.  
- **Examples:** Swap label at each hop.  

---

### 3. Path Forwarding (Step 3)  
- **Function:** Packet follows a predefined Label Switched Path (LSP).  
- **Role:** Ensures predictable routing path.  
- **Examples:** Traffic engineering routes.  

---

### 4. Label Removal (Step 4)  
- **Function:** Egress router removes label before final delivery.  
- **Role:** Packet returns to normal IP routing.  
- **Examples:** Sending packet to destination network.  

---

## Key MPLS Components  
- **Label:** Short identifier replacing IP lookup.  
- **LSP (Label Switched Path):** Predefined path for packets.  
- **Ingress Router:** Entry point adding label.  
- **Egress Router:** Exit point removing label.  

---

## Why It Matters  
- **Performance:** Faster than traditional routing.  
- **Traffic Engineering:** Controls path selection.  
- **QoS Support:** Prioritizes traffic efficiently.  

---

## Quick Recap (Mnemonic)  
- **Assign → Switch → Forward → Remove**  
  - **Label → Hop → Path → Deliver**  

---


# THANK YOU!  
# ~ **V1NNN22**