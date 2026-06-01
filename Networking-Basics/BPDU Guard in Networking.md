# BPDU Guard in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is BPDU Guard?  
- **Definition:** BPDU Guard is a Spanning Tree Protocol (STP) security feature that automatically disables a port if it receives a BPDU packet unexpectedly.  
- **Purpose:** Prevents unauthorized switches from affecting the network topology.  
- **Simple Meaning:** If a user port starts acting like a switch, shut it down.  

---  

## The 4 Core Steps of BPDU Guard  

### 1. PortFast Enabled (Step 1)  
- **Function:** Port is configured for end devices.  
- **Role:** Expected to connect only PCs, printers, or servers.  

---  

### 2. BPDU Received (Step 2)  
- **Function:** Switch receives a BPDU packet on that port.  
- **Role:** Indicates another switch may be connected.  

---  

### 3. Violation Detected (Step 3)  
- **Function:** BPDU Guard identifies unexpected STP traffic.  
- **Role:** Protects network topology.  

---  

### 4. Port Shutdown (Step 4)  
- **Function:** Port enters Err-Disabled state.  
- **Result:** Unauthorized switch is blocked immediately.  

---  

## Why BPDU Guard Exists  
- **Stops rogue switches**  
- **Prevents STP manipulation**  
- **Protects root bridge election**  
- **Avoids accidental loops**  

---  

## Real-World Attack Without BPDU Guard  

### Attacker Connects Switch
```text
Priority = 0
```

### Result
```text
Attacker becomes Root Bridge
```

### Impact
- Traffic rerouting
- Network instability
- Possible MITM attacks

---  

## Detection  

### Check Err-Disabled Ports
```bash
show interfaces status err-disabled
```

---

### Check BPDU Guard Status
```bash
show spanning-tree summary
```

---  

## Configuration Example  

### Enable PortFast
```bash
spanning-tree portfast
```

---

### Enable BPDU Guard
```bash
spanning-tree bpduguard enable
```

---

### Global Configuration
```bash
spanning-tree portfast bpduguard default
```

---  

## What Happens After Violation?  

### Port State
```text
Err-Disabled
```

### Recovery
```bash
shutdown
no shutdown
```

---  

## Key Features  
- STP security feature  
- Blocks rogue switches  
- Automatic protection  
- Prevents topology manipulation  

---  

## Why It Matters  
- **Protects Layer 2 infrastructure**  
- **Prevents accidental loops**  
- **Maintains STP stability**  
- **Critical enterprise security control**  

---  

## Quick Recap  
**Connect → Receive BPDU → Detect → Shutdown**  
**PortFast → BPDU → Violation → Protect**  

---  

# THANK YOU!  
# ~ **V1NNN22**