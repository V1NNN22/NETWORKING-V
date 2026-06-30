# MPLS LDP (Label Distribution Protocol) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is LDP?  
- **Definition:** Label Distribution Protocol (LDP) is an MPLS protocol used by routers to exchange and assign labels for forwarding packets.
- **Purpose:** Automatically build Label Switched Paths (LSPs).
- **Simple Meaning:** Routers agree on which label should be used for each destination.

---

## The 4 Core Steps of LDP

### 1. Neighbor Discovery (Step 1)
- **Function:** MPLS routers discover nearby LDP peers.
- **Role:** Establish communication.

---

### 2. Session Establishment (Step 2)
- **Function:** Routers create an LDP session.
- **Role:** Exchange label information.

---

### 3. Label Exchange (Step 3)
- **Function:** Routers advertise labels for IP prefixes.
- **Role:** Build Label Forwarding Information Base (LFIB).

---

### 4. MPLS Forwarding (Step 4)
- **Function:** Packets are forwarded using labels instead of IP lookups.
- **Result:** Fast and efficient forwarding.

---

## Why LDP Exists

### Automates
```text
Label Distribution
```

### Builds
```text
Label Switched Paths (LSPs)
```

### Improves
```text
MPLS Efficiency
```

---

## Real-World Example

### Router A
```text
Prefix 10.1.1.0/24
Label 100
```

↓

### Router B
```text
Learns Label 100
```

↓

### Router C
```text
Forwards using Label 100
```

---

## Packet Flow

### Ingress
```text
Push Label
```

↓

### Core
```text
Swap Label
```

↓

### Egress
```text
Pop Label
```

---

## Detection

### View LDP Neighbors
```bash
show mpls ldp neighbor
```

---

### View LDP Bindings
```bash
show mpls ldp bindings
```

---

### View MPLS Table
```bash
show mpls forwarding-table
```

---

## Configuration Example

### Enable MPLS
```bash
mpls ip
```

---

### Enable LDP
```bash
mpls label protocol ldp
```

---

## Advantages

### Automatic
```text
No manual labels
```

### Scalable
```text
Large MPLS networks
```

### Reliable
```text
Stable label exchange
```

---

## Drawbacks

### Shortest Path Only
```text
Uses IGP decisions
```

### No Traffic Engineering
```text
Cannot optimize paths
```

---

## LDP vs RSVP-TE

### LDP
```text
Automatic Labels
Shortest Path
```

### RSVP-TE
```text
Traffic Engineering
Explicit Path Control
```

---

## Key Features
- Automatic label exchange
- MPLS control protocol
- Builds LSPs
- Uses IGP topology

---

## Why It Matters
- **Foundation of MPLS**
- **Used by ISPs**
- **Simplifies MPLS deployment**
- **Essential MPLS protocol**

---

## Quick Recap
**Discover → Connect → Exchange → Forward**
**LDP → Labels → LSP → MPLS**

---

# THANK YOU!
# ~ **V1NNN22**