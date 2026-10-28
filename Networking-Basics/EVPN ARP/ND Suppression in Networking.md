---

# EVPN ARP/ND Suppression in Networking  
~
## Written By: VINOD N. RATHOD.  
~

## What is EVPN ARP/ND Suppression?  
- **Definition:** EVPN ARP/ND Suppression is a feature used in Ethernet VPN (EVPN) networks to reduce unnecessary ARP and IPv6 Neighbor Discovery (ND) broadcast or multicast traffic.
- **Purpose:** It allows a network device, such as a Virtual Tunnel Endpoint (VTEP), to answer certain address-resolution requests using IP-to-MAC information learned through the EVPN control plane.
- **Analogy:** Imagine asking an entire apartment building who owns a particular car. Instead, the building manager checks a directory and gives you the answer directly.

---  

## The 4 Core Steps of EVPN ARP/ND Suppression Operation  

### 1. Learn IP-to-MAC Information  
- **Function:** A VTEP learns host IP and MAC address information from locally connected devices.
- **Role:** This information can be advertised to other VTEPs through EVPN control-plane routes.
- **Examples:** A VTEP learns that IP `192.168.1.10` belongs to MAC address `AA:BB:CC:DD:EE:FF`.

---  

### 2. Advertise Information Through EVPN  
- **Function:** The VTEP advertises the relevant MAC and IP reachability information using EVPN, commonly through a MAC/IP Advertisement route (Route Type 2).
- **Role:** Remote VTEPs can build a directory of known host addresses without relying entirely on network-wide ARP or ND flooding.
- **Examples:** A remote VTEP learns the IP-to-MAC mapping for a host connected to another VTEP.

---  

### 3. Intercept Address-Resolution Requests  
- **Function:** When a host sends an ARP request or IPv6 Neighbor Solicitation, the local VTEP checks whether it has a valid matching entry.
- **Role:** The VTEP can answer using its learned information instead of flooding the request across the overlay.
- **Examples:** A host asks for the MAC address associated with `192.168.1.10`, and the VTEP finds the mapping in its EVPN database.

---  

### 4. Respond or Forward the Request  
- **Function:** If a valid mapping is available and suppression is enabled, the VTEP can provide a local response. Otherwise, the request may be forwarded or flooded according to network configuration.
- **Role:** This preserves address resolution while reducing unnecessary overlay traffic.
- **Examples:** A VTEP answers an ARP request locally when it knows the destination MAC address.

---  

## Key Features  
- **Reduced Flooding:** Limits unnecessary ARP and IPv6 ND traffic across the overlay.
- **Control-Plane Learning:** Uses IP-to-MAC information distributed through EVPN.
- **IPv4 and IPv6 Support:** Can suppress ARP requests and applicable IPv6 Neighbor Discovery requests.
- **Improved Scalability:** Helps large Layer 2 overlay networks handle address resolution more efficiently.
- **Mapping Dependency:** Accurate entries and correct configuration are essential for reliable suppression.

---  

## Why It Matters  
- **Less Network Traffic:** Reduces repeated address-resolution broadcasts and multicasts.
- **Better Overlay Efficiency:** Helps reduce unnecessary traffic between VTEPs.
- **Large Data Center Support:** Useful in EVPN-VXLAN fabrics with many hosts and segments.
- **Faster Resolution:** A local response can avoid waiting for a request to travel across the overlay.

---  

## Quick Recap (Mnemonic)  
- **Learn → Advertise → Check → Respond**  
  - **Learn host mapping → Share through EVPN → Check incoming requests → Answer locally when possible**  

---  


# THANK YOU!  
# ~ **V1NNN22**