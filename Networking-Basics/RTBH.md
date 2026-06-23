# Remote Triggered Black Hole (RTBH) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is RTBH?  
- **Definition:** Remote Triggered Black Hole (RTBH) is a DDoS mitigation technique that uses BGP to instruct upstream routers to discard traffic before it reaches the victim network.
- **Purpose:** Stop attack traffic as close to the source as possible.
- **Simple Meaning:** Tell your ISP to drop the traffic before it even reaches you.

---

## The 4 Core Steps of RTBH

### 1. Attack Detection (Step 1)
- **Function:** A DDoS attack is detected.
- **Role:** Trigger mitigation process.

---

### 2. Blackhole Route Injection (Step 2)
- **Function:** A special BGP route is advertised.
- **Role:** Marks target IP for traffic dropping.

---

### 3. Upstream Propagation (Step 3)
- **Function:** ISP receives the blackhole community.
- **Role:** Installs discard route.

---

### 4. Traffic Dropped Upstream (Step 4)
- **Function:** Attack packets are discarded before reaching victim.
- **Result:** Network bandwidth is protected.

---

## Why RTBH Exists

### Traditional Blackholing
```text
Traffic reaches your network first
```

### RTBH
```text
Traffic dropped at ISP edge
```

### Result
```text
Bandwidth preserved
```

---

## Real-World Example

### Victim
```text
203.0.113.10
```

### Attack
```text
800 Gbps DDoS
```

### RTBH Route
```text
203.0.113.10/32
Community: Blackhole
```

### Result
```text
Traffic dropped upstream
```

---

## How RTBH Works

### Normal Routing
```text
Internet → ISP → Victim
```

### During Attack
```text
Internet → ISP → Null0
```

### Outcome
```text
Victim protected
```

---

## Common BGP Community

### Example
```text
65535:666
```

### Meaning
```text
Blackhole this route
```

(Note: Community values vary by ISP.)

---

## Detection

### View BGP Communities
```bash
show ip bgp community
```

---

### View BGP Routes
```bash
show ip bgp
```

Look for:
```text
Blackhole Community
```

---

## Configuration Example

### Static Route
```bash
ip route 203.0.113.10 255.255.255.255 Null0
```

---

### Apply Community
```bash
set community 65535:666
```

---

### Advertise Route
```bash
network 203.0.113.10 mask 255.255.255.255
```

---

## Types of RTBH

### Destination RTBH
```text
Drop traffic to victim
```

### Source RTBH
```text
Drop traffic from attacker
```

---

## Advantages

### Protects Bandwidth
```text
Attack never reaches you
```

### Fast Mitigation
```text
Seconds to activate
```

### ISP Support
```text
Widely available
```

---

## Drawbacks

### Service Unavailable
```text
Victim becomes unreachable
```

### All Traffic Dropped
```text
Good and bad traffic
```

---

## RTBH vs BGP Blackholing

### BGP Blackholing
```text
Drop traffic in your network
```

### RTBH
```text
Drop traffic in ISP network
```

---

## Key Features
- Upstream mitigation
- BGP community based
- DDoS protection
- Bandwidth preservation

---

## Why It Matters
- **Protects against massive DDoS attacks**
- **Prevents circuit saturation**
- **Common ISP security service**
- **Essential incident response tool**

---

## Quick Recap
**Detect → Signal → Propagate → Drop**
**Attack → BGP Community → ISP Action → Protection**

---

# THANK YOU!
# ~ **V1NNN22**