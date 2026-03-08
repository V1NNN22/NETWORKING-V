# BGP (Border Gateway Protocol)  
~
## Written By: VINOD N. RATHOD.  
~

## What is BGP?  
- **Definition:** A path-vector routing protocol used to exchange routing information between different autonomous systems (AS) on the internet.  
- **Purpose:** Determines the best path for data across large-scale networks → enables communication between ISPs and global networks.  
- **Analogy:** Like international flight routing where airlines decide the best path between countries.  

---

## The 4 Core Steps of BGP Operation  

### 1. BGP Neighbor Establishment (Step 1)  
- **Function:** Two routers establish a TCP connection to become BGP peers.  
- **Role:** Enables exchange of routing information.  
- **Examples:** TCP port 179 used for BGP communication.  

---

### 2. Route Advertisement (Step 2)  
- **Function:** Routers share reachable network prefixes with neighbors.  
- **Role:** Announces which networks can be reached through them.  
- **Examples:** Advertising IP prefix like `192.0.2.0/24`.  

---

### 3. Path Selection (Step 3)  
- **Function:** Router evaluates multiple routes and selects the best one.  
- **Role:** Uses attributes such as AS path, local preference, and MED.  
- **Examples:** Shortest AS path preferred.  

---

### 4. Route Propagation (Step 4)  
- **Function:** Selected best route is shared with other BGP peers.  
- **Role:** Builds global internet routing tables.  
- **Examples:** ISP sharing routes with upstream providers.  

---

## Key BGP Attributes  
- **AS Path:** Sequence of autonomous systems a route passes through.  
- **Local Preference:** Preferred outbound path within an AS.  
- **MED (Multi Exit Discriminator):** Suggests preferred entry point to an AS.  
- **Next Hop:** IP address of next router for reaching destination.  

---

## Why It Matters  
- **Internet Backbone Routing:** Core protocol connecting ISPs globally.  
- **Scalability:** Handles massive global routing tables.  
- **Policy-Based Routing:** Allows organizations to control traffic paths.  

---

## Quick Recap (Mnemonic)  
- **Peer → Advertise → Select → Propagate**  
  - **Neighbor → Route → Best Path → Global Routing**  

---

# THANK YOU!  
# ~ **V1NNN22**