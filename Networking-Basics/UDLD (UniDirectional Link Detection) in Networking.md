# UDLD (UniDirectional Link Detection) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is UDLD?  
- **Definition:** UDLD is a Layer 2 protocol that detects unidirectional communication on fiber and Ethernet links.
- **Purpose:** Prevents network issues caused by one-way links.
- **Simple Meaning:** Makes sure both ends of a link can hear each other.

---

## The 4 Core Steps of UDLD

### 1. Neighbor Discovery (Step 1)
- **Function:** Devices exchange UDLD packets.
- **Role:** Verify bidirectional communication.

---

### 2. Link Monitoring (Step 2)
- **Function:** Devices continuously monitor received UDLD messages.
- **Role:** Ensure both sides remain reachable.

---

### 3. Unidirectional Detection (Step 3)
- **Function:** One side stops receiving UDLD packets.
- **Role:** Identifies one-way communication failure.

---

### 4. Port Protection (Step 4)
- **Function:** UDLD disables the affected port.
- **Result:** Prevents loops and STP issues.

---

## Why UDLD Exists
- **Detects fiber failures**
- **Prevents Layer 2 loops**
- **Protects STP topology**
- **Improves link reliability**

---

## Real-World Problem Without UDLD

### Fiber Issue
```text
Switch A → Switch B = Works
Switch B → Switch A = Fails
```

### Result
```text
One-way communication
```

### Impact
- STP instability
- Broadcast storms
- Traffic blackholing
- Network outages

---

## Detection

### Check UDLD Status
```bash
show udld
```

---

### Check Interface Status
```bash
show udld interface
```

---

## Configuration Example

### Enable UDLD Globally
```bash
udld enable
```

---

### Enable Aggressive Mode
```bash
udld aggressive
```

---

### Per Interface
```bash
interface g0/1
udld port aggressive
```

---

## Normal vs Aggressive Mode

### Normal Mode
```text
Detects problem
Reports event
```

### Aggressive Mode
```text
Detects problem
Err-disables port
```

---

## Key Features
- Detects one-way links
- Works at Layer 2
- Common on fiber links
- Prevents STP problems

---

## Why It Matters
- **Prevents silent link failures**
- **Protects network stability**
- **Reduces downtime**
- **Critical in redundant networks**

---

## Quick Recap
**Discover → Monitor → Detect → Disable**
**UDLD → Check → Failure → Protect**

---

# THANK YOU!
# ~ **V1NNN22**