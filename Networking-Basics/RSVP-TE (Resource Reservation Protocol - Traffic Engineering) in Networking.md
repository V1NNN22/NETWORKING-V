# RSVP-TE (Resource Reservation Protocol - Traffic Engineering) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is RSVP-TE?  
- **Definition:** RSVP-TE is an MPLS protocol that creates Label Switched Paths (LSPs) with explicit routes and reserved bandwidth.
- **Purpose:** Enable Traffic Engineering (TE) by controlling exactly how traffic flows through the network.
- **Simple Meaning:** Instead of taking the shortest road, choose the best road.

---

## The 4 Core Steps of RSVP-TE

### 1. Path Calculation (Step 1)
- **Function:** Router calculates the desired path.
- **Role:** Avoid congestion or reserve bandwidth.

---

### 2. Resource Reservation (Step 2)
- **Function:** RSVP reserves bandwidth along the selected path.
- **Role:** Guarantee available resources.

---

### 3. LSP Establishment (Step 3)
- **Function:** MPLS labels are assigned along the path.
- **Role:** Create a Traffic Engineering tunnel.

---

### 4. Traffic Forwarding (Step 4)
- **Function:** Packets follow the reserved path.
- **Result:** Predictable and optimized traffic flow.

---

## Why RSVP-TE Exists

### Avoid
```text
Congested Links
```

### Reserve
```text
Bandwidth
```

### Control
```text
Traffic Paths
```

---

## Real-World Example

### Shortest Path
```text
A → B → C → D
```

### Congested
```text
B → C
```

### RSVP-TE Path
```text
A → E → F → D
```

### Result
```text
Better Performance
```

---

## Packet Flow

### Path Message
```text
Reserve Route
```

↓

### RESV Message
```text
Confirm Reservation
```

↓

### MPLS Tunnel
```text
Ready
```

---

## Detection

### View RSVP Neighbors
```bash
show ip rsvp neighbor
```

---

### View TE Tunnels
```bash
show mpls traffic-eng tunnels
```

---

### View RSVP Sessions
```bash
show ip rsvp interface
```

---

## Configuration Example

### Enable Traffic Engineering
```bash
mpls traffic-eng tunnels
```

---

### Enable RSVP
```bash
ip rsvp bandwidth
```

---

### Create Tunnel
```bash
interface Tunnel0
tunnel mode mpls traffic-eng
```

---

## Advantages

### Bandwidth Reservation
```text
Guaranteed Resources
```

### Explicit Routing
```text
Choose Exact Path
```

### Fast Reroute
```text
Rapid Failure Recovery
```

---

## Drawbacks

### Complex Configuration
```text
More Management
```

### State Information
```text
Higher Memory Usage
```

---

## RSVP-TE vs LDP

### LDP
```text
Shortest Path
No Bandwidth Reservation
```

### RSVP-TE
```text
Explicit Path
Bandwidth Reservation
```

---

## Key Features
- Traffic Engineering
- Bandwidth Reservation
- Explicit Routing
- MPLS Tunnel Creation

---

## Why It Matters
- **Optimizes network utilization**
- **Avoids congestion**
- **Guarantees bandwidth**
- **Essential for service provider MPLS networks**

---

## Quick Recap
**Calculate → Reserve → Establish → Forward**
**Path → RSVP → Tunnel → Optimized Traffic**

---

# THANK YOU!
# ~ **V1NNN22**