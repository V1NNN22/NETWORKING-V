# CAM Table Exhaustion in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is CAM Table Exhaustion?  
- **Definition:** CAM Table Exhaustion is an attack where a switch’s MAC address table is flooded with fake MAC addresses until it becomes full.  
- **Purpose (Attack):** Forces switch to behave like a hub.  
- **Simple Meaning:** Overload the switch memory so it starts broadcasting traffic everywhere.  

---  

## The 4 Core Steps of CAM Table Exhaustion  

### 1. Fake MAC Flooding (Step 1)  
- **Function:** Attacker sends frames with thousands of fake MAC addresses.  
- **Role:** Fills switch CAM table rapidly.  

---  

### 2. CAM Table Full (Step 2)  
- **Function:** Switch cannot learn new legitimate MAC addresses.  
- **Result:** Memory capacity exhausted.  

---  

### 3. Unknown Unicast Flooding (Step 3)  
- **Function:** Switch starts broadcasting unknown traffic to all ports.  
- **Role:** Behaves similar to old hub devices.  

---  

### 4. Traffic Sniffing (Step 4)  
- **Function:** Attacker captures traffic not meant for them.  
- **Result:** Packet sniffing and possible MITM attacks.  

---  

## Why CAM Table Exhaustion Happens  
- **Limited CAM memory**  
- **No port security enabled**  
- **Layer 2 trust assumption**  
- **Cheap unmanaged switches**  

---  

## Real-World Impact  
- **Traffic leakage**  
- **Sensitive data exposure**  
- **MITM opportunities**  
- **Network instability**  
- **Switch CPU stress**  

---  

## Detection  
```bash
show mac address-table
```

Check:  
- Huge number of random MAC addresses  
- Rapid MAC learning changes  

---

### Packet Capture  
```bash
tcpdump -i eth0
```

Check for:  
- Unexpected broadcasted unicast traffic  

---  

## Common Attack Tool  
```bash
macof
```

From:  
```bash
dsniff toolkit
```

---  

## Protection Methods  

### Enable Port Security  
```bash
switchport port-security
```

---

### Limit MAC Addresses  
```bash
switchport port-security maximum 5
```

---

### Sticky MAC Learning  
```bash
switchport port-security mac-address sticky
```

---  

## Key Features  
- Layer 2 attack  
- Exploits switch MAC learning  
- Turns switch into pseudo-hub  
- Common in internal network attacks  

---  

## Why It Matters  
- **Traffic interception risk**  
- **Network confidentiality loss**  
- **Important for switch hardening**  
- **Critical in enterprise security**  

---  

## Quick Recap  
**Flood → Fill → Broadcast → Sniff**  
**Fake MAC → CAM Full → Hub Mode → Capture**  

---  

# THANK YOU!  
# ~ **V1NNN22**