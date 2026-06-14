# PMTUD (Path MTU Discovery) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is PMTUD?  
- **Definition:** Path MTU Discovery (PMTUD) is a mechanism that determines the largest packet size that can travel across a network path without fragmentation.
- **Purpose:** Optimize packet delivery and avoid fragmentation.
- **Simple Meaning:** Find the biggest packet that fits through every network device on the path.

---

## The 4 Core Steps of PMTUD

### 1. Large Packet Sent (Step 1)
- **Function:** Sender transmits packets with the DF (Don't Fragment) flag set.
- **Role:** Prevent routers from fragmenting packets.

---

### 2. MTU Limitation Found (Step 2)
- **Function:** Router encounters a packet larger than its interface MTU.
- **Role:** Cannot forward the packet.

---

### 3. ICMP Notification (Step 3)
- **Function:** Router sends an ICMP "Fragmentation Needed" message.
- **Role:** Informs sender about the MTU limitation.

---

### 4. Packet Size Adjustment (Step 4)
- **Function:** Sender reduces packet size.
- **Result:** Packets successfully reach destination.

---

## Why PMTUD Exists
- **Avoids fragmentation**
- **Improves efficiency**
- **Reduces router workload**
- **Optimizes end-to-end performance**

---

## Real-World Example

### Sender MTU
```text
1500 Bytes
```

### VPN Tunnel MTU
```text
1400 Bytes
```

### Result
```text
Packets dropped
```

### PMTUD Action
```text
Sender lowers packet size
```

---

## Problem Without PMTUD

### Large Packets
```text
Cannot pass through path
```

### Result
```text
Packet loss
Slow applications
Connection issues
```

---

## Detection

### Linux
```bash
tracepath google.com
```

---

### Windows
```bash
ping -f -l 1472 google.com
```

---

### Packet Capture
```bash
tcpdump icmp
```

Look for:
```text
Fragmentation Needed
```

---

## Common MTU Values

### Ethernet
```text
1500 Bytes
```

### PPPoE
```text
1492 Bytes
```

### VXLAN
```text
1450 Bytes (Typical)
```

### Jumbo Frames
```text
9000 Bytes
```

---

## PMTUD Black Hole

### Cause
```text
ICMP messages blocked
```

### Result
```text
Sender never learns MTU
```

### Impact
```text
Connections stall
```

---

## Key Features
- Discovers path MTU
- Prevents fragmentation
- Uses ICMP feedback
- Improves efficiency

---

## Why It Matters
- **Critical for VPNs**
- **Important in cloud networks**
- **Improves application performance**
- **Reduces packet fragmentation**

---

## Quick Recap
**Send → Drop → Notify → Adjust**
**DF Flag → ICMP → Smaller Packet → Success**

---

# THANK YOU!
# ~ **V1NNN22**