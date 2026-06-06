# Route Poisoning in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is Route Poisoning?  
- **Definition:** Route Poisoning is a routing technique used to mark a failed route as unreachable by assigning it an infinite metric.
- **Purpose:** Prevents routers from using bad routes and helps stop routing loops.
- **Simple Meaning:** Tell everyone, "This route is dead. Don't use it."

---

## The 4 Core Steps of Route Poisoning

### 1. Route Failure (Step 1)
- **Function:** A network becomes unreachable.
- **Role:** Trigger routing update.

---

### 2. Infinite Metric Assignment (Step 2)
- **Function:** Router marks route with maximum metric.
- **Role:** Indicates route is unusable.

---

### 3. Route Advertisement (Step 3)
- **Function:** Poisoned route is advertised to neighbors.
- **Role:** Spread failure information quickly.

---

### 4. Route Removal (Step 4)
- **Function:** Neighboring routers remove bad route.
- **Result:** Loop prevention and convergence.

---

## Why Route Poisoning Exists
- **Prevents routing loops**
- **Speeds up convergence**
- **Avoids stale routes**
- **Improves routing stability**

---

## Real-World Problem Without Route Poisoning

### Network Failure
```text
192.168.10.0/24 Down
```

### Router Belief
```text
Route still exists
```

### Result
```text
Traffic sent into black hole
```

### Impact
- Packet loss
- Routing loops
- Slow convergence

---

## Example (RIP)

### Normal Route
```text
192.168.10.0 Metric 2
```

### Poisoned Route
```text
192.168.10.0 Metric 16
```

### Meaning
```text
Unreachable
```

---

## Detection

### Check Routing Table
```bash
show ip route
```

---

### Check RIP Updates
```bash
debug ip rip
```

---

## Related Concepts

### Route Poisoning
```text
Marks route as dead
```

### Split Horizon
```text
Prevents route from returning
```

### Poison Reverse
```text
Advertises failed route back
```

---

## Common Routing Protocols

### Uses Route Poisoning
```text
RIP
EIGRP
```

---

### Less Relevant
```text
OSPF
IS-IS
```

(Link-state protocols use different mechanisms.)

---

## Key Features
- Infinite metric assignment
- Loop prevention
- Faster convergence
- Routing stability

---

## Why It Matters
- **Reduces routing loops**
- **Prevents black holes**
- **Improves fault recovery**
- **Essential routing concept**

---

## Quick Recap
**Fail → Poison → Advertise → Remove**
**Dead Route → Infinite Metric → Notify → Converge**

---

# THANK YOU!
# ~ **V1NNN22**