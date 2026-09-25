---

# QinQ (802.1Q-in-802.1Q) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is QinQ?  
- **Definition:** QinQ, also called VLAN stacking, places an additional 802.1Q VLAN tag around an existing VLAN-tagged Ethernet frame.
- **Purpose:** It allows service providers to transport customer VLANs across a shared Layer 2 network without modifying the customer's original VLAN tags.
- **Analogy:** Like putting a customer's sealed package inside a second delivery box with the courier company's own routing label.

---  

## The 4 Core Steps of QinQ Operation  

### 1. Customer VLAN Tagging  
- **Function:** The customer network sends normal 802.1Q-tagged Ethernet frames.
- **Role:** Identifies the customer's internal VLAN.
- **Examples:** A customer frame may contain VLAN `100` as its inner tag.

---  

### 2. Service VLAN Tag Insertion  
- **Function:** The provider network adds an outer VLAN tag to the customer frame.
- **Role:** Separates and identifies customer traffic within the provider network.
- **Examples:** The provider adds outer VLAN `2000` while preserving the customer's VLAN `100`.

---  

### 3. Provider Network Transport  
- **Function:** Provider switches forward the double-tagged frame using the outer VLAN tag.
- **Role:** Carries multiple customer VLANs through the provider infrastructure.
- **Examples:** VLANs `100`, `200`, and `300` from one customer can travel inside the same service VLAN `2000`.

---  

### 4. Outer Tag Removal  
- **Function:** The provider edge removes the outer service VLAN tag before delivering the frame to the customer network.
- **Role:** Restores the original customer VLAN frame.
- **Examples:** The customer receives the original VLAN `100` frame without needing to understand the provider's outer VLAN.

---  

## Key Features  
- **VLAN Stacking:** Uses multiple VLAN tags on a single Ethernet frame.
- **Customer Isolation:** Separates customer traffic within provider infrastructure.
- **VLAN Transparency:** Preserves the customer's original VLAN information.
- **Scalability:** Allows providers to transport many customer VLANs.

---  

## Why It Matters  
- **Service Provider Networks:** Enables Layer 2 VPN and Ethernet services.
- **Enterprise Connectivity:** Connects geographically separated customer sites.
- **VLAN Reuse:** Different customers can use overlapping internal VLAN IDs.
- **Network Scalability:** Reduces the need to manage every customer VLAN individually.

---  

## Quick Recap (Mnemonic)  
- **C → A → T → R**  
  - **Customer Tag → Add Service Tag → Transport → Remove Outer Tag**  

---  


# THANK YOU!  
# ~ **V1NNN22**