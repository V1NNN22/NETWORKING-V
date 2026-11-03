---

# IS-IS Prefix-SID in Segment Routing  
~
## Written By: VINOD N. RATHOD.  
~

## What is IS-IS Prefix-SID?  
- **Definition:** IS-IS Prefix Segment Identifier (Prefix-SID) is a Segment Routing identifier advertised through IS-IS that represents a specific network prefix.
- **Purpose:** It allows routers to forward traffic toward a destination prefix using Segment Routing instructions instead of relying solely on traditional label-switched path signaling.
- **Analogy:** Imagine a delivery system where every destination has a unique code. Routers use that code to determine how to move a package toward its destination.

---  

## The 4 Core Steps of IS-IS Prefix-SID Operation  

### 1. Prefix-SID Configuration  
- **Function:** A Prefix-SID is assigned to an IGP prefix, commonly a loopback address.
- **Role:** The SID represents the forwarding instruction associated with reaching that prefix.
- **Examples:** Router R1 assigns Prefix-SID `16001` to its loopback prefix `10.0.0.1/32`.

---  

### 2. Prefix-SID Advertisement  
- **Function:** IS-IS advertises the prefix and its Prefix-SID using Segment Routing extensions.
- **Role:** Other routers learn the association between the destination prefix and its SID.
- **Examples:** R2 receives IS-IS information indicating that Prefix-SID `16001` represents the route to `10.0.0.1/32`.

---  

### 3. SID-to-Label Mapping  
- **Function:** In SR-MPLS, routers interpret a Prefix-SID using the Segment Routing Global Block (SRGB) and the SID value.
- **Role:** The mapping determines the MPLS label used to represent the segment.
- **Examples:** With an SRGB starting at `16000`, a Prefix-SID index of `1` maps to label `16001`.

---  

### 4. Segment-Based Forwarding  
- **Function:** A router forwards packets using the label associated with the Prefix-SID.
- **Role:** The network follows the shortest path toward the prefix according to the applicable IGP topology and metric.
- **Examples:** R2 pushes label `16001` and forwards the packet toward R1 along the IS-IS shortest path.

---  

## Key Features  
- **Prefix-Based SID:** Associates a segment identifier with an IGP prefix.
- **IS-IS Signaling:** Advertises Prefix-SID information through IS-IS.
- **SR-MPLS Support:** Enables label-based Segment Routing forwarding.
- **Global SID Behavior:** A Prefix-SID index can have consistent meaning across routers using a common SRGB.
- **IGP Integration:** Uses IS-IS topology and metrics for path computation.

---  

## Why It Matters  
- **Simplifies MPLS Traffic Engineering:** Supports Segment Routing without requiring LDP for label distribution.
- **Scalable Forwarding:** Routers can use segment identifiers to direct traffic.
- **Efficient Path Selection:** Leverages the IGP shortest-path topology.
- **Network Programmability:** Prefix-SIDs can be combined with other segments to create engineered paths.

---  

## Quick Recap (Mnemonic)  
- **Assign → Advertise → Map → Forward**  
  - **Assign SID to prefix → Share through IS-IS → Resolve SID to label → Forward toward destination**  

---  


# THANK YOU!  
# ~ **V1NNN22**