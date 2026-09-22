---

# DHCP Starvation Attack in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is DHCP Starvation Attack?  
- **Definition:** A DHCP starvation attack is a network attack where an attacker sends a large number of DHCP requests using different or spoofed client identifiers, attempting to consume all available IP addresses in the DHCP pool.
- **Purpose:** It prevents legitimate devices from obtaining IP addresses and can disrupt network connectivity.
- **Analogy:** Like someone repeatedly taking numbered tokens from a limited queue until genuine customers have none left.

---  

## The 4 Core Steps of DHCP Starvation Attack  

### 1. DHCP Request Generation  
- **Function:** The attacker generates many DHCP discovery/request messages.
- **Role:** Creates the appearance of numerous different clients requesting network configuration.
- **Examples:** An attacker may rapidly generate requests using changing MAC addresses.

---  

### 2. Address Pool Consumption  
- **Function:** The DHCP server allocates available addresses to the apparent clients.
- **Role:** Gradually exhausts the DHCP address pool.
- **Examples:** A `/24` DHCP scope with limited available addresses can become fully allocated.

---  

### 3. Legitimate Client Failure  
- **Function:** Genuine devices attempt to obtain an address but find no available lease.
- **Role:** Causes users to lose normal network access.
- **Examples:** A new laptop may fail to obtain a valid IPv4 address from DHCP.

---  

### 4. Detection and Mitigation  
- **Function:** Network security controls identify abnormal DHCP request rates and limit suspicious traffic.
- **Role:** Restores availability and prevents repeated pool exhaustion.
- **Examples:** DHCP snooping, port security, rate limiting, and appropriate DHCP scope monitoring can help mitigate the attack.

---  

## Key Features  
- **Resource Exhaustion:** Targets the finite DHCP address pool.
- **Identity Spoofing:** May use many different client identifiers or MAC addresses.
- **Availability Attack:** Primarily affects the ability of legitimate clients to obtain addresses.
- **Layer 2 Security Controls:** Switch-level protections can help detect or restrict suspicious DHCP behavior.

---  

## Why It Matters  
- **Network Availability:** Can prevent legitimate devices from joining the network.
- **Security Awareness:** Demonstrates why DHCP infrastructure needs protection.
- **Incident Detection:** Unusual DHCP request volumes can indicate suspicious activity.
- **Defense Planning:** Encourages proper use of DHCP snooping, rate limits, and port controls.

---  

## Quick Recap (Mnemonic)  
- **R → C → F → P**  
  - **Requests → Consume Pool → Fail Legitimate Clients → Protect**  

---  


# THANK YOU!  
# ~ **V1NNN22**