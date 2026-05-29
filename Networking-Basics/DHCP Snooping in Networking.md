# DHCP Snooping in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is DHCP Snooping?  
- **Definition:** DHCP Snooping is a Layer 2 security feature that filters DHCP messages and blocks unauthorized DHCP servers.  
- **Purpose:** Prevents rogue DHCP attacks.  
- **Simple Meaning:** Switch acts like a security guard for DHCP traffic.  

---  

## The 4 Core Steps of DHCP Snooping  

### 1. Port Classification (Step 1)  
- **Function:** Switch marks ports as Trusted or Untrusted.  
- **Role:** Defines who can send DHCP offers.  

---  

### 2. DHCP Request (Step 2)  
- **Function:** Client broadcasts DHCP Discover.  
- **Role:** Searches for an IP address.  

---  

### 3. DHCP Validation (Step 3)  
- **Function:** Switch checks DHCP replies.  
- **Role:** Ensures offers come from trusted ports only.  

---  

### 4. DHCP Assignment (Step 4)  
- **Function:** Valid DHCP response reaches client.  
- **Result:** Client gets legitimate network settings.  

---  

## Why DHCP Snooping Exists  
- **Blocks rogue DHCP servers**  
- **Prevents fake gateway attacks**  
- **Protects clients from malicious IP assignments**  
- **Creates trusted IP-MAC database**  

---  

## Real-World Impact  
- **Stops MITM attacks**  
- **Prevents network hijacking**  
- **Improves Layer 2 security**  
- **Protects enterprise environments**  

---  

## Common Attack Without DHCP Snooping  

### Attacker DHCP Server
```text
Gateway: 192.168.1.200
DNS: Evil Server
```

### Result
- Traffic passes through attacker
- Credentials can be captured
- Users may not notice anything

---  

## Detection  

### Check Snooping Status
```bash
show ip dhcp snooping
```

---

### View Binding Table
```bash
show ip dhcp snooping binding
```

---  

## Configuration Example  

### Enable DHCP Snooping
```bash
ip dhcp snooping
```

---

### Enable on VLAN
```bash
ip dhcp snooping vlan 10
```

---

### Trust Uplink Port
```bash
interface g0/1
ip dhcp snooping trust
```

---  

## Key Features  
- Blocks rogue DHCP servers  
- Builds IP-MAC binding table  
- Layer 2 security feature  
- Works with other security mechanisms  

---  

## Why It Matters  
- **Prevents DHCP-based attacks**  
- **Protects users automatically**  
- **Foundation for DAI and IP Source Guard**  
- **Essential enterprise security control**  

---  

## Quick Recap  
**Classify → Request → Validate → Assign**  
**Trust → DHCP → Verify → Secure**  

---  

# THANK YOU!  
# ~ **V1NNN22**