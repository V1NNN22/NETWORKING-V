---

# Segment Routing Global Block (SRGB) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is Segment Routing Global Block (SRGB)?  
- **Definition:** The Segment Routing Global Block (SRGB) is a range of MPLS label values reserved by a Segment Routing router for its globally significant prefix SIDs.
- **Purpose:** It allows routers to map Prefix Segment Identifiers (Prefix-SIDs) to MPLS labels and forward traffic toward specific destinations without maintaining traditional per-flow label-switched paths.
- **Analogy:** Like a standardized numbering system that allows different offices to identify the same destination using a consistent reference number.

---  

## The 4 Core Steps of SRGB Operation  

### 1. SRGB Range Configuration  
- **Function:** An administrator configures an MPLS label range as the router's SRGB.
- **Role:** Defines the labels available for mapping global Prefix-SIDs.
- **Examples:** A router uses labels `16000–23999` as its SRGB.

---  

### 2. Prefix-SID Assignment  
- **Function:** A Prefix-SID is assigned to a network prefix, commonly using an index value.
- **Role:** Identifies a destination within the Segment Routing domain.
- **Examples:** A router advertises Prefix-SID index `10` for its loopback prefix.

---  

### 3. Label Mapping  
- **Function:** Each router maps the Prefix-SID index to an MPLS label using its own SRGB.
- **Role:** Converts the global SID into a locally meaningful label value.
- **Examples:** With an SRGB starting at `16000`, Prefix-SID index `10` maps to label `16010`.

---  

### 4. Label-Based Forwarding  
- **Function:** Routers use the mapped MPLS label to forward packets along the path toward the destination.
- **Role:** Enables segment-based forwarding through the network.
- **Examples:** An ingress router pushes the label associated with the destination Prefix-SID, and transit routers forward the packet toward the destination.

---  

## Key Features  
- **Label Range:** Defines a block of labels reserved for global Prefix-SID mapping.
- **Index-Based Mapping:** Converts Prefix-SID indices into MPLS labels.
- **IGP Integration:** Prefix-SIDs and SRGB information can be advertised through IS-IS or OSPF extensions.
- **Segment Routing Support:** Enables MPLS-based Segment Routing without requiring a separate label-distribution protocol for these SIDs.

---  

## Why It Matters  
- **Simplified Traffic Engineering:** Prefix-SIDs provide a consistent way to identify destinations.
- **Scalable Forwarding:** Supports segment-based paths through large provider networks.
- **Reduced Signaling:** Avoids needing a separate label-distribution protocol for Segment Routing Prefix-SIDs.
- **Network Automation:** Provides a structured label-mapping scheme across routers.

---  

## Quick Recap (Mnemonic)  
- **R → S → M → F**  
  - **Reserve Range → Assign SID → Map Label → Forward Packet**  

---  


# THANK YOU!  
# ~ **V1NNN22**