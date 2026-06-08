# Poison Reverse in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is Poison Reverse?  
- **Definition:** Poison Reverse is a routing loop prevention technique where a router advertises a learned route back to the neighbor it learned it from, but marks it as unreachable.
- **Purpose:** Explicitly tells neighbors not to use that route through it.
- **Simple Meaning:** "I learned this route from you, so don't try to reach it through me."

---

## The 4 Core Steps of Poison Reverse

### 1. Route Learning (Step 1)
- **Function:** Router learns a route from a neighbor.
- **Role:** Adds route to routing table.

---

### 2. Route Failure Risk (Step 2)
- **Function:** Potential routing loop may occur.
- **Role:** Router prepares loop prevention.

---

### 3. Poison Advertisement (Step 3)
- **Function:** Router advertises route back with infinite metric.
- **Role:** Marks route as unreachable.

---

### 4. Loop Prevention (Step 4)
- **Function:** Neighbor ignores that path.
- **Result:** Routing loop avoided.

---

## Why Poison Reverse Exists
- **Prevents routing loops**
- **Improves convergence**
- **Provides explicit route rejection**
- **Enhances distance-vector stability**

---

## Real-World Problem Without Poison Reverse

### Router A
```text
Route X Available
```

### Link Failure
```text
Route X Lost
```

### Router B Thinks
```text
Router A still has Route X
```

### Result
```text
Packets loop endlessly
```

---

## Example

### Normal Route
```text
192.168.10.0 Metric 2
```

### Poison Reverse
```text
192.168.10.0 Metric 16
```

### Meaning
```text
Route Unreachable
```

---

## Detection

### RIP Updates
```bash
debug ip rip
```

---

### Routing Table
```bash
show ip route
```

---

## Split Horizon vs Poison Reverse

### Split Horizon
```text
Do not advertise route back
```

### Poison Reverse
```text
Advertise route back as unreachable
```

---

## Common Protocols

### Uses Poison Reverse
```text
RIP
EIGRP (similar concepts)
```

---

## Key Features
- Loop prevention
- Explicit route rejection
- Faster convergence
- Distance-vector enhancement

---

## Why It Matters
- **Reduces routing loops**
- **Improves network stability**
- **Speeds failure recovery**
- **Important routing mechanism**

---

## Quick Recap
**Learn → Poison → Advertise → Prevent**
**Route → Infinite Metric → Notify → Safe**

---

# THANK YOU!
# ~ **V1NNN22**