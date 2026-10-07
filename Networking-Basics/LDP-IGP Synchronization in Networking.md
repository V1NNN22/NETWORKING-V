---

# LDP-IGP Synchronization in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is LDP-IGP Synchronization?

- **Definition:** LDP-IGP Synchronization is a mechanism that helps ensure MPLS label distribution is ready before an IGP such as OSPF or IS-IS starts using a link for normal traffic.
- **Purpose:** To prevent packet loss caused by an IGP forwarding traffic over a link before the corresponding MPLS labels are properly established.
- **Analogy:** Think of a railway opening a new track only after both the track and its signaling system are ready. Having the track alone is not enough unless trains can safely follow the signals.

---  

## The 4 Core Steps of LDP-IGP Synchronization Operation

### 1. IGP Link Discovery (Step 1)
- **Function:** The IGP discovers a neighboring router and establishes the link as part of the routing topology.
- **Role:** Provides the underlying path that MPLS traffic may use.
- **Examples:** OSPF or IS-IS discovers an adjacent MPLS router.

---  

### 2. LDP Neighbor Establishment (Step 2)
- **Function:** LDP establishes a session with the neighboring router and begins exchanging label information.
- **Role:** Builds the label-switched forwarding information required for MPLS traffic.
- **Examples:** Router A establishes an LDP session with Router B over an OSPF-enabled link.

---  

### 3. Synchronization Check (Step 3)
- **Function:** The router checks whether the required LDP label information is available for the link.
- **Role:** Prevents the IGP from immediately preferring a link whose MPLS forwarding state is not ready.
- **Examples:** A newly restored link may remain less preferred until LDP synchronization completes.

---  

### 4. IGP Preference Restoration (Step 4)
- **Function:** Once LDP is synchronized, the router removes the temporary IGP penalty or condition.
- **Role:** Allows the link to participate normally in shortest-path routing.
- **Examples:** After labels are exchanged successfully, the restored MPLS link becomes eligible for normal traffic.

---  

## Key Features
- **MPLS Protection:** Helps prevent forwarding inconsistencies between IGP and LDP.
- **Temporary IGP Adjustment:** Can reduce the preference of an unsynchronized link.
- **Loss Prevention:** Reduces the chance of traffic entering a path without corresponding labels.
- **Service Provider Use:** Commonly relevant in MPLS networks using LDP with OSPF or IS-IS.

---  

## Why It Matters
- **Reliable Convergence:** Keeps routing and label forwarding aligned during topology changes.
- **Reduced Packet Loss:** Helps avoid traffic being sent through an MPLS path before labels are ready.
- **Operational Stability:** Useful when links or routers recover after failures.
- **Better MPLS Resilience:** Coordinates the control planes responsible for routing and label forwarding.

---  

## Quick Recap (Mnemonic)
- **Discover → Label → Synchronize → Restore**
  - **Discover link → Establish LDP → Check labels → Restore normal IGP preference**

---  

# THANK YOU!
# ~ **V1NNN22**