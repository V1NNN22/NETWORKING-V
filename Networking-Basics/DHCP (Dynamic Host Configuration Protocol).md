# DHCP (Dynamic Host Configuration Protocol)  
~
## Written By: VINOD N. RATHOD.  
~

## What is DHCP?  
- **Definition:** A network management protocol that automatically assigns IP addresses and other network configuration details to devices on a network.  
- **Purpose:** Eliminates manual IP configuration → reduces errors and simplifies large network management.  
- **Analogy:** Like a hotel reception assigning room numbers and access cards to guests automatically.  

---

## The 4-Step DHCP Process (DORA)  

### 1. Discover (Step 1)  
- **Function:** Client broadcasts a request to find a DHCP server.  
- **Role:** Initiates IP address allocation process.  
- **Examples:** New laptop connects to WiFi and sends DHCP Discover.  

---

### 2. Offer (Step 2)  
- **Function:** DHCP server responds with an available IP address.  
- **Role:** Proposes configuration details (IP, Subnet Mask, Gateway, DNS).  
- **Examples:** Server offers 192.168.1.25.  

---

### 3. Request (Step 3)  
- **Function:** Client requests the offered IP address.  
- **Role:** Confirms acceptance of configuration.  
- **Examples:** Client replies “I accept 192.168.1.25.”  

---

### 4. Acknowledge (Step 4)  
- **Function:** Server confirms and assigns the IP officially.  
- **Role:** Finalizes configuration and lease time.  
- **Examples:** DHCP ACK packet with lease duration (e.g., 24 hours).  

---

## Key DHCP Components  
- **IP Address:** Unique identifier for device.  
- **Subnet Mask:** Defines network range.  
- **Default Gateway:** Router IP for external communication.  
- **DNS Server:** Resolves domain names.  
- **Lease Time:** Duration for IP assignment.  

---

## Why It Matters  
- **Automation:** No need for manual IP setup.  
- **Scalability:** Supports large enterprise networks.  
- **Error Reduction:** Prevents IP conflicts.  

---

## Quick Recap (Mnemonic)  
- **Discover → Offer → Request → Acknowledge**  
  - **D → O → R → A (DORA Process)**  

---

# THANK YOU!  
# ~ **V1NNN22**