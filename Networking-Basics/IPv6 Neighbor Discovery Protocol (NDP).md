---

# IPv6 Neighbor Discovery Protocol (NDP)  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is IPv6 Neighbor Discovery Protocol?  
- **Definition:** A set of IPv6 mechanisms used by hosts and routers to discover neighbors, routers, prefixes, and link-layer addresses.  
- **Purpose:** Performs several functions that ARP, ICMP Router Discovery, and related mechanisms provide in IPv4.  
- **Analogy:** Like a neighborhood directory that helps devices discover who is nearby, who the local gateway is, and where everyone lives.  

---  

## The 4 Core Steps of NDP Operation  

### 1. Router Discovery (Step 1)  
- **Function:** Hosts discover available IPv6 routers on the local network.  
- **Role:** Helps devices identify their default gateway and learn network information.  
- **Examples:** A host receives a Router Advertisement containing prefix and configuration information.  

---  

### 2. Neighbor Discovery (Step 2)  
- **Function:** IPv6 devices discover the link-layer address of neighboring devices.  
- **Role:** Allows hosts to determine where local IPv6 traffic should be delivered.  
- **Examples:** A Neighbor Solicitation is used to resolve a neighbor's IPv6 address to its MAC address.  

---  

### 3. Address Configuration (Step 3)  
- **Function:** Hosts can learn network prefixes and configure IPv6 addresses automatically.  
- **Role:** Reduces the need for manual address configuration.  
- **Examples:** A device uses information from Router Advertisements to generate an IPv6 address.  

---  

### 4. Reachability Detection (Step 4)  
- **Function:** Devices verify whether neighboring nodes remain reachable.  
- **Role:** Helps maintain accurate neighbor information and detect connectivity changes.  
- **Examples:** Neighbor Unreachability Detection determines whether a previously reachable neighbor has stopped responding.  

---  

## Key Features  
- **Router Discovery:** Identifies IPv6 routers and default gateways.  
- **Neighbor Resolution:** Maps IPv6 addresses to link-layer addresses.  
- **Auto Configuration:** Supports automatic IPv6 address configuration.  
- **Reachability Detection:** Tracks whether neighboring devices remain reachable.  

---  

## Why It Matters  
- **IPv6 Connectivity:** Provides essential mechanisms for communication on IPv6 networks.  
- **Automation:** Enables devices to configure themselves with minimal manual intervention.  
- **Network Discovery:** Helps hosts understand their local IPv6 environment.  
- **Efficiency:** Uses multicast-based communication instead of IPv4-style broadcast mechanisms.  

---  

## Quick Recap (Mnemonic)  
- **Discover → Resolve → Configure → Verify**  
  - **Router → Neighbor → Address → Reachability**  

---  


# THANK YOU!  
# ~ **V1NNN22**