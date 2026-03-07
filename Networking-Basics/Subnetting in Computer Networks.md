# Subnetting in Computer Networks  
~
## Written By: VINOD N. RATHOD.  
~

## What is Subnetting?  
- **Definition:** A network design technique that divides a large IP network into smaller logical networks called subnets.  
- **Purpose:** Improves network efficiency, security, and address management by organizing IP ranges into manageable segments.  
- **Analogy:** Like dividing a large apartment building into separate floors and rooms for better organization.  

---

## The 4 Core Steps of Subnetting  

### 1. Identify Network Requirements (Step 1)  
- **Function:** Determine number of required subnets and hosts per subnet.  
- **Role:** Helps decide how many bits should be borrowed from host portion.  
- **Examples:** Network needing 4 subnets with 50 hosts each.  

---

### 2. Borrow Host Bits (Step 2)  
- **Function:** Convert host bits into network bits in subnet mask.  
- **Role:** Creates multiple subnet identifiers.  
- **Examples:** Changing /24 network to /26 subnet mask.  

---

### 3. Calculate Subnet Ranges (Step 3)  
- **Function:** Determine subnet IDs, usable host ranges, and broadcast addresses.  
- **Role:** Defines boundaries for each subnet.  
- **Examples:**  
  - Subnet 1: 192.168.1.0 – 192.168.1.63  
  - Subnet 2: 192.168.1.64 – 192.168.1.127  

---

### 4. Assign Subnets to Network Segments (Step 4)  
- **Function:** Allocate each subnet to different departments or network segments.  
- **Role:** Improves traffic control and network organization.  
- **Examples:** HR network, Finance network, IT network.  

---

## Key Subnetting Components  
- **Network Address:** First IP in subnet identifying the network.  
- **Usable Host Range:** IP addresses assignable to devices.  
- **Broadcast Address:** Last IP used to communicate with all hosts in subnet.  
- **Subnet Mask / CIDR:** Defines boundary between network and host bits.  

---

## Why It Matters  
- **Efficient IP Usage:** Reduces wasted IP addresses.  
- **Improved Security:** Isolates network segments.  
- **Better Traffic Management:** Limits broadcast domains.  

---

## Quick Recap (Mnemonic)  
- **Plan → Borrow → Calculate → Assign**  
  - **Requirement → Subnet Mask → Address Range → Network Allocation**  

---

# THANK YOU!  
# ~ **V1NNN22**