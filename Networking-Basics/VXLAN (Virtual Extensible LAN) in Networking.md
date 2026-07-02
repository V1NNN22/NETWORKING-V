# VXLAN (Virtual Extensible LAN) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is VXLAN?  
- **Definition:** VXLAN is a Layer 2 overlay technology that encapsulates Ethernet frames inside UDP packets, allowing Layer 2 networks to extend across Layer 3 networks.
- **Purpose:** Build scalable virtual networks for cloud and data centers.
- **Simple Meaning:** Carry an Ethernet network through an IP network.

---

## The 4 Core Steps of VXLAN

### 1. Frame Encapsulation (Step 1)
- **Function:** VTEP encapsulates Ethernet frame into a VXLAN packet.
- **Role:** Add VXLAN and UDP headers.

---

### 2. Layer 3 Transport (Step 2)
- **Function:** Packet travels across the IP network.
- **Role:** Underlay network forwards using IP routing.

---

### 3. Decapsulation (Step 3)
- **Function:** Destination VTEP removes VXLAN headers.
- **Role:** Restore original Ethernet frame.

---

### 4. Local Delivery (Step 4)
- **Function:** Ethernet frame reaches destination host.
- **Result:** Devices behave as if on the same LAN.

---

## Why VXLAN Exists

### VLAN Limit
```text
4096 VLANs
```

### VXLAN
```text
16 Million VNIs
```

### Result
```text
Massive Scalability
```

---

## Real-World Example

### VM 1
```text
Data Center A
```

↓

### IP Network
```text
Internet/MPLS
```

↓

### VM 2
```text
Data Center B
```

### Result
```text
Same Layer 2 Network
```

---

## VXLAN Header

### Ethernet Frame
```text
Original Packet
```

↓

### VXLAN Header
```text
VNI Added
```

↓

### UDP Header
```text
Port 4789
```

↓

### IP Header
```text
Underlay Routing
```

---

## Detection

### View VXLAN Interface
```bash
show interface vxlan
```

---

### View VTEPs
```bash
show nve peers
```

---

### View VXLAN Tunnel
```bash
show vxlan
```

---

## Configuration Example

### Create VXLAN Interface
```bash
interface nve1
```

---

### Configure Source
```bash
source-interface Loopback0
```

---

### Map VNI
```bash
member vni 10010
```

---

## Components

### VTEP
```text
VXLAN Tunnel Endpoint
```

### VNI
```text
VXLAN Network Identifier
```

### Underlay
```text
IP Network
```

### Overlay
```text
Virtual Layer 2 Network
```

---

## Advantages

### Scalability
```text
16 Million Networks
```

### Flexibility
```text
Works Across Layer 3
```

### Cloud Ready
```text
Supports VM Mobility
```

---

## Drawbacks

### Overhead
```text
Extra Headers
```

### MTU Requirement
```text
Larger Packet Size
```

---

## VXLAN vs VLAN

### VLAN
```text
4096 Networks
Layer 2 Only
```

### VXLAN
```text
16 Million VNIs
Runs Over Layer 3
```

---

## Key Features
- Layer 2 Overlay
- UDP Encapsulation
- VTEP-Based Tunneling
- Highly Scalable

---

## Why It Matters
- **Foundation of modern data centers**
- **Enables cloud networking**
- **Supports VM migration**
- **Critical for large-scale virtualization**

---

## Quick Recap
**Encapsulate → Transport → Decapsulate → Deliver**
**Ethernet → VXLAN → IP Network → Ethernet**

---

# THANK YOU!
# ~ **V1NNN22**