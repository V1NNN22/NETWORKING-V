# Root Guard in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is Root Guard?  
- **Definition:** Root Guard is an STP security feature that prevents a port from becoming a path to a new Root Bridge.  
- **Purpose:** Ensures the intended switch remains the Root Bridge.  
- **Simple Meaning:** Stops another switch from taking over as the STP boss.  

---  

## The 4 Core Steps of Root Guard  

### 1. Root Bridge Selected (Step 1)  
- **Function:** Network elects a Root Bridge.  
- **Role:** Central reference point for STP.  

---  

### 2. Superior BPDU Received (Step 2)  
- **Function:** Port receives a BPDU claiming a better Root Bridge.  
- **Role:** Indicates another switch wants control.  

---  

### 3. Root Guard Triggered (Step 3)  
- **Function:** Switch blocks the port from influencing STP.  
- **Role:** Protects current Root Bridge.  

---  

### 4. Root-Inconsistent State (Step 4)  
- **Function:** Port is placed into a special blocked state.  
- **Result:** New Root Bridge is rejected.  

---  

## Why Root Guard Exists  
- **Prevents rogue Root Bridges**  
- **Maintains STP design**  
- **Protects topology stability**  
- **Stops accidental switch misconfigurations**  

---  

## Real-World Attack Without Root Guard  

### Attacker Switch
```text
Priority = 0
```

### Result
```text
Becomes Root Bridge
```

### Impact
- Traffic path changes
- Unpredictable routing
- Possible interception opportunities

---  

## Detection  

### Check Root Guard Status
```bash
show spanning-tree inconsistentports
```

---

### Check STP Information
```bash
show spanning-tree
```

---  

## Configuration Example  

### Enable Root Guard
```bash
interface g0/1
spanning-tree guard root
```

---  

## What Happens During Violation?  

### Port State
```text
Root-Inconsistent
```

### Recovery
```text
Automatic when superior BPDU stops
```

No manual intervention required.

---  

## BPDU Guard vs Root Guard  

### BPDU Guard
```text
Receives Any BPDU = Shutdown
```

### Root Guard
```text
Receives Superior BPDU = Block
```

---  

## Key Features  
- STP protection feature  
- Prevents Root Bridge takeover  
- Automatic recovery  
- Preserves network design  

---  

## Why It Matters  
- **Keeps STP stable**  
- **Protects network architecture**  
- **Prevents topology hijacking**  
- **Important for enterprise switching**  

---  

## Quick Recap  
**Root Exists → Superior BPDU → Block → Protect**  
**STP → Challenge → Root Guard → Safe**  

---  

# THANK YOU!  
# ~ **V1NNN22**