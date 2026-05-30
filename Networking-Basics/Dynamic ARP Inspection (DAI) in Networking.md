# Dynamic ARP Inspection (DAI) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is Dynamic ARP Inspection (DAI)?  
- **Definition:** DAI is a Layer 2 security feature that validates ARP packets before allowing them through the network.  
- **Purpose:** Prevents ARP Spoofing and ARP Poisoning attacks.  
- **Simple Meaning:** Switch checks if an ARP message is telling the truth.  

---  

## The 4 Core Steps of DAI  

### 1. ARP Packet Received (Step 1)  
- **Function:** Switch receives an ARP request or reply.  
- **Role:** Begins inspection process.  

---  

### 2. Database Verification (Step 2)  
- **Function:** Switch compares ARP information with DHCP Snooping database.  
- **Role:** Checks IP-to-MAC legitimacy.  

---  

### 3. Validation Decision (Step 3)  
- **Function:** Switch verifies whether ARP packet is valid.  
- **Result:** Pass or Drop.  

---  

### 4. Traffic Protection (Step 4)  
- **Function:** Valid ARP packets continue through network.  
- **Result:** Spoofed packets are blocked.  

---  

## Why DAI Exists  
- **Stops ARP spoofing attacks**  
- **Prevents Man-in-the-Middle (MITM)**  
- **Protects gateway MAC mappings**  
- **Maintains ARP table integrity**  

---  

## Real-World Attack Without DAI  

### Attacker Sends
```text
192.168.1.1 = AA:AA:AA:AA:AA:AA
```

### Victim Believes
```text
Default Gateway = Attacker MAC
```

### Result
- Traffic redirected
- Credentials intercepted
- Session hijacking possible

---  

## Detection  

### Check DAI Status
```bash
show ip arp inspection
```

---

### View Statistics
```bash
show ip arp inspection statistics
```

---

### Check Dropped Packets
```bash
show ip arp inspection interfaces
```

---  

## Configuration Example  

### Enable DAI
```bash
ip arp inspection vlan 10
```

---

### Trust Uplink Port
```bash
interface g0/1
ip arp inspection trust
```

---  

## Requirements  
- DHCP Snooping enabled  
- DHCP Snooping binding table available  
- Trusted uplink ports configured  

---  

## Key Features  
- Layer 2 protection  
- Blocks ARP poisoning  
- Uses DHCP Snooping database  
- Protects gateway identity  

---  

## Why It Matters  
- **Prevents MITM attacks**  
- **Protects sensitive traffic**  
- **Maintains network trust**  
- **Essential enterprise security feature**  

---  

## Quick Recap  
**Receive → Verify → Validate → Protect**  
**ARP → Check → Pass/Drop → Secure**  

---  

# THANK YOU!  
# ~ **V1NNN22**