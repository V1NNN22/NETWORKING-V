# IP Source Guard in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is IP Source Guard?  
- **Definition:** IP Source Guard (IPSG) is a Layer 2 security feature that prevents IP address spoofing by allowing traffic only from valid IP-MAC combinations.  
- **Purpose:** Blocks devices from using fake IP addresses.  
- **Simple Meaning:** A device can only use the IP address assigned to it.  

---  

## The 4 Core Steps of IP Source Guard  

### 1. IP Assignment (Step 1)  
- **Function:** Client receives an IP address from DHCP.  
- **Role:** DHCP Snooping records the IP-MAC mapping.  

---  

### 2. Binding Creation (Step 2)  
- **Function:** Switch builds a trusted binding table.  
- **Role:** Stores valid IP-MAC-Port information.  

---  

### 3. Packet Inspection (Step 3)  
- **Function:** Switch checks outgoing packets.  
- **Role:** Verifies source IP against binding table.  

---  

### 4. Traffic Decision (Step 4)  
- **Function:** Valid packets are forwarded.  
- **Result:** Spoofed packets are dropped.  

---  

## Why IP Source Guard Exists  
- **Prevents IP spoofing**  
- **Protects network identity**  
- **Stops unauthorized devices**  
- **Enhances access security**  

---  

## Real-World Attack Without IPSG  

### Attacker Changes IP
```text
Real IP: 192.168.1.50
Fake IP: 192.168.1.1
```

### Result
- Bypass restrictions
- Impersonate trusted hosts
- Launch network attacks

---  

## Detection  

### Check Binding Table
```bash
show ip dhcp snooping binding
```

---

### Check IPSG Status
```bash
show ip verify source
```

---  

## Configuration Example  

### Enable DHCP Snooping
```bash
ip dhcp snooping
```

---

### Enable Source Guard
```bash
interface g0/10
ip verify source
```

---  

## Requirements  
- DHCP Snooping enabled  
- DHCP Snooping binding table available  
- Access port configuration  

---  

## Key Features  
- Blocks IP spoofing  
- Uses DHCP Snooping database  
- Per-port validation  
- Layer 2 security feature  

---  

## Why It Matters  
- **Prevents identity spoofing**  
- **Protects enterprise networks**  
- **Reduces attack surface**  
- **Complements DAI and DHCP Snooping**  

---  

## Security Trio  

### DHCP Snooping
```text
Who gives the IP?
```

### DAI
```text
Who owns the IP?
```

### IP Source Guard
```text
Who is using the IP?
```

---  

## Quick Recap  
**Assign → Bind → Verify → Allow**  
**DHCP → Table → Check → Secure**  

---  

# THANK YOU!  
# ~ **V1NNN22**