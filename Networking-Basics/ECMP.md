# ECMP (Equal-Cost Multi-Path) Routing in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is ECMP?  
- **Definition:** ECMP is a routing technique that allows traffic to be forwarded across multiple paths that have the same routing cost.
- **Purpose:** Improve bandwidth utilization and provide redundancy.
- **Simple Meaning:** Use multiple equally good roads instead of just one.

---

## The 4 Core Steps of ECMP

### 1. Route Discovery (Step 1)
- **Function:** Router learns multiple paths to the same destination.
- **Role:** All paths have equal metric.

---

### 2. Path Installation (Step 2)
- **Function:** Router installs multiple routes into the routing table.
- **Role:** Creates multiple forwarding options.

---

### 3. Traffic Hashing (Step 3)
- **Function:** Router uses a hashing algorithm.
- **Role:** Determines which path a flow will use.

---

### 4. Load Distribution (Step 4)
- **Function:** Traffic is spread across available paths.
- **Result:** Better utilization and resilience.

---

## Why ECMP Exists
- **Load balancing**
- **Redundancy**
- **Higher throughput**
- **Efficient path utilization**

---

## Real-World Example

### Destination
```text
10.10.10.0/24
```

### Available Paths
```text
Path A Cost 10
Path B Cost 10
Path C Cost 10
```

### Result
```text
Traffic distributed across all paths
```

---

## How ECMP Chooses a Path

### Common Hash Inputs
```text
Source IP
Destination IP
Source Port
Destination Port
Protocol
```

### Purpose
```text
Keep same flow on same path
```

---

## Detection

### Routing Table
```bash
show ip route
```

---

### CEF Table
```bash
show ip cef
```

---

### BGP ECMP
```bash
show ip bgp
```

---

## Configuration Example

### OSPF ECMP
```bash
maximum-paths 4
```

---

### EIGRP ECMP
```bash
maximum-paths 4
```

---

### BGP ECMP
```bash
maximum-paths 4
```

---

## Benefits

### Performance
```text
Better bandwidth usage
```

### Reliability
```text
Automatic failover
```

### Scalability
```text
Supports large networks
```

---

## Potential Challenges

### Uneven Traffic
```text
Hash imbalance
```

### Out-of-Order Packets
```text
Per-packet ECMP
```

### Troubleshooting
```text
More complex paths
```

---

## ECMP vs Load Balancer

### ECMP
```text
Layer 3 Routing
```

### Load Balancer
```text
Layer 4/7 Distribution
```

---

## Key Features
- Multiple equal-cost paths
- Traffic distribution
- Fast failover
- Protocol independent

---

## Why It Matters
- **Maximizes bandwidth**
- **Improves availability**
- **Essential in data centers**
- **Common in ISP networks**

---

## Quick Recap
**Learn → Install → Hash → Forward**
**Equal Cost → Multiple Paths → Load Share → Fast Network**

---

# THANK YOU!
# ~ **V1NNN22**