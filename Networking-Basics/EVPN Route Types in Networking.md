---

# EVPN Route Types in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What are EVPN Route Types?  
- **Definition:** EVPN (Ethernet VPN) route types are different BGP message formats used to advertise MAC addresses, IP addresses, network membership, and forwarding information across an EVPN network.
- **Purpose:** They allow network devices to discover endpoints and exchange the information required to forward traffic across VXLAN or MPLS-based Layer 2 networks.
- **Analogy:** Like different types of notices in a building: one identifies residents, another announces available rooms, and another provides directions between buildings.

---  

## The 4 Core Steps of EVPN Route Type Operation  

### 1. Ethernet Auto-Discovery (Type 1)  
- **Function:** Advertises Ethernet segment membership and supports functions such as mass withdrawal and aliasing.
- **Role:** Helps maintain connectivity and redundancy when multiple provider-edge devices connect to the same Ethernet segment.
- **Examples:** If one PE device fails, other devices can update forwarding behavior for the affected Ethernet segment.

---  

### 2. MAC/IP Advertisement (Type 2)  
- **Function:** Advertises endpoint MAC addresses and optionally their associated IP addresses.
- **Role:** Helps remote VTEPs or PE devices learn where endpoints are reachable.
- **Examples:** A leaf switch advertises a virtual machine's MAC address and IP address to other leaf switches.

---  

### 3. Inclusive Multicast Ethernet Tag (Type 3)  
- **Function:** Advertises participation in an EVPN broadcast domain and supports the discovery of remote VTEPs for BUM traffic.
- **Role:** Helps establish the distribution of broadcast, unknown-unicast, and multicast traffic.
- **Examples:** A VTEP advertises that it participates in VNI `10010`, allowing other participating VTEPs to discover it.

---  

### 4. Ethernet Segment and IP Prefix Routes (Types 4 and 5)  
- **Function:** Type 4 supports Ethernet Segment discovery and Designated Forwarder election, while Type 5 advertises IP prefixes.
- **Role:** Supports multihoming coordination and Layer 3 reachability between networks.
- **Examples:** Type 4 helps coordinate forwarding across a multihomed segment, while Type 5 advertises a subnet reachable through a remote EVPN gateway.

---  

## Key Features  
- **BGP-Based Signaling:** Uses BGP to distribute EVPN reachability information.
- **MAC/IP Learning:** Shares endpoint information between network devices.
- **Multihoming Support:** Enables redundant connections to multiple PE devices.
- **Layer 3 Integration:** Type 5 routes support IP prefix advertisement.

---  

## Why It Matters  
- **Data Center Fabrics:** Supports scalable EVPN-VXLAN architectures.
- **Endpoint Mobility:** Helps update reachability when virtual machines move between hosts.
- **Network Redundancy:** Supports multihoming and resilient forwarding.
- **Multi-Tenant Networking:** Enables isolated Layer 2 and Layer 3 services across shared infrastructure.

---  

## Quick Recap (Mnemonic)  
- **T1 → T2 → T3 → T4/T5**  
  - **Auto-Discovery → MAC/IP Learning → Multicast Membership → Multihoming/IP Prefixes**  

---  


# THANK YOU!  
# ~ **V1NNN22**