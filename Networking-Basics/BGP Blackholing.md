# BGP Blackholing in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is BGP Blackholing?  
- **Definition:** BGP Blackholing is a technique used to intentionally discard traffic destined for a specific IP address or network prefix.
- **Purpose:** Mitigate DDoS attacks and protect network infrastructure.
- **Simple Meaning:** Send unwanted traffic into a digital black hole where it disappears forever.

---

## The 4 Core Steps of BGP Blackholing

### 1. Attack Detection (Step 1)
- **Function:** Network identifies malicious traffic.
- **Role:** Trigger mitigation process.

---

### 2. Blackhole Route Creation (Step 2)
- **Function:** Special BGP route is generated.
- **Role:** Marks target destination for dropping.

---

### 3. Route Advertisement (Step 3)
- **Function:** Blackhole route is propagated.
- **Role:** Inform routers to discard traffic.

---

### 4. Traffic Discarded (Step 4)
- **Function:** Packets matching target are dropped.
- **Result:** Attack traffic never reaches victim.

---

## Why BGP Blackholing Exists

### DDoS Protection
```text
Stop attack traffic
```

### Infrastructure Protection
```text
Prevent network overload
```

### Fast Response
```text
Mitigate attacks quickly
```

---

## Real-World Example

### Victim Server
```text
203.0.113.10
```

### DDoS Traffic
```text
500 Gbps Attack
```

### Blackhole Route
```text
203.0.113.10/32 → Null0
```

### Result
```text
Traffic dropped
```

---

## How Blackholing Works

### Normal Route
```text
Destination → Server
```

### Blackhole Route
```text
Destination → Null0
```

### Outcome
```text
Packet discarded
```

---

## Detection

### View BGP Routes
```bash
show ip bgp
```

---

### Check Null Routes
```bash
show ip route
```

Look for:
```text
Null0
```

---

## Configuration Example

### Static Null Route
```bash
ip route 203.0.113.10 255.255.255.255 Null0
```

---

### Advertise via BGP
```bash
network 203.0.113.10 mask 255.255.255.255
```

---

## Types of Blackholing

### Local Blackhole
```text
Traffic dropped locally
```

### Remote Triggered Black Hole (RTBH)
```text
Traffic dropped upstream
```

---

## Advantages

### Fast Mitigation
```text
Seconds to deploy
```

### Network Protection
```text
Reduce congestion
```

### Simple Design
```text
Easy implementation
```

---

## Drawbacks

### Collateral Damage
```text
Legitimate traffic dropped
```

### Service Impact
```text
Target becomes unreachable
```

---

## BGP Blackholing vs Firewall

### Firewall
```text
Filter specific traffic
```

### Blackholing
```text
Drop all traffic
```

---

## Key Features
- DDoS mitigation
- Traffic discard mechanism
- Fast deployment
- ISP-friendly solution

---

## Why It Matters
- **Protects against large attacks**
- **Reduces infrastructure stress**
- **Common ISP defense technique**
- **Essential DDoS response tool**

---

## Quick Recap
**Detect → Advertise → Redirect → Drop**
**Attack → Blackhole Route → Null0 → Protection**

---

# THANK YOU!
# ~ **V1NNN22**