# Split Horizon in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is Split Horizon?  
- **Definition:** Split Horizon is a loop prevention technique where a router does not advertise a route back out of the interface from which it learned it.
- **Purpose:** Prevents routing loops in distance-vector protocols.
- **Simple Meaning:** Don't tell someone information they originally told you.

---

## The 4 Core Steps of Split Horizon

### 1. Route Learning (Step 1)
- **Function:** Router learns a route from a neighbor.
- **Role:** Stores route in routing table.

---

### 2. Routing Update Creation (Step 2)
- **Function:** Router prepares updates for neighbors.
- **Role:** Determines which routes to advertise.

---

### 3. Split Horizon Check (Step 3)
- **Function:** Router checks source interface of learned route.
- **Role:** Prevents route from being advertised back.

---

### 4. Safe Advertisement (Step 4)
- **Function:** Route is sent only to other interfaces.
- **Result:** Routing loops are avoided.

---

## Why Split Horizon Exists
- **Prevents routing loops**
- **Improves network stability**
- **Reduces unnecessary updates**
- **Speeds up convergence**

---

## Real-World Problem Without Split Horizon

### Router A
```text
Learns Route X
```

### Router B
```text
Learns Route X from Router A
```

### Issue
```text
Router B advertises Route X back to Router A
```

### Result
```text
Routing loop forms
```

---

## Example

### Learned Route
```text
192.168.10.0/24 via Interface G0/0
```

### Split Horizon Rule
```text
Do NOT advertise it back via G0/0
```

---

## Detection

### Check Routing Updates
```bash
debug ip rip
```

---

### Check Interface Settings
```bash
show ip protocols
```

---

## Configuration Example

### Disable Split Horizon
```bash
interface g0/0
no ip split-horizon
```

### Enable Split Horizon
```bash
interface g0/0
ip split-horizon
```

---

## Split Horizon vs Route Poisoning

### Split Horizon
```text
Do not advertise route back
```

### Route Poisoning
```text
Advertise route as unreachable
```

---

## Common Routing Protocols

### Uses Split Horizon
```text
RIP
EIGRP
```

### Not Required
```text
OSPF
IS-IS
```

(Link-state protocols use topology databases.)

---

## Key Features
- Loop prevention mechanism
- Distance-vector protection
- Reduces routing traffic
- Simple and effective

---

## Why It Matters
- **Stops routing loops**
- **Improves network reliability**
- **Reduces unnecessary updates**
- **Fundamental routing concept**

---

## Quick Recap
**Learn → Check → Block → Advertise**
**Route In → Same Interface → Don't Send Back → Safe**

---

# THANK YOU!
# ~ **V1NNN22**