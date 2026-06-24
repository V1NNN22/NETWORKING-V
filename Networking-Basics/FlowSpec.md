# BGP FlowSpec in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is BGP FlowSpec?  
- **Definition:** BGP FlowSpec is an extension to BGP that distributes traffic filtering rules across routers using BGP updates.
- **Purpose:** Mitigate DDoS attacks and enforce traffic policies dynamically.
- **Simple Meaning:** Send firewall rules through BGP.

---

## The 4 Core Steps of BGP FlowSpec

### 1. Attack Detection (Step 1)
- **Function:** Malicious traffic is identified.
- **Role:** Trigger mitigation action.

---

### 2. Flow Rule Creation (Step 2)
- **Function:** A FlowSpec rule is generated.
- **Role:** Define what traffic to match.

---

### 3. BGP Advertisement (Step 3)
- **Function:** Rule is distributed via BGP.
- **Role:** Share mitigation policy across routers.

---

### 4. Traffic Filtering (Step 4)
- **Function:** Routers apply the rule.
- **Result:** Malicious traffic is blocked or rate-limited.

---

## Why BGP FlowSpec Exists

### Traditional Method
```text
Configure ACLs manually
```

### FlowSpec Method
```text
Push rules automatically
```

### Result
```text
Faster mitigation
```

---

## Real-World Example

### DDoS Traffic
```text
UDP Port 53 Flood
```

### FlowSpec Rule
```text
Match UDP
Destination Port 53
Drop Traffic
```

### Result
```text
Attack blocked network-wide
```

---

## What Can FlowSpec Match?

### Source IP
```text
Attacker Address
```

### Destination IP
```text
Victim Address
```

### Protocol
```text
TCP
UDP
ICMP
```

### Port Numbers
```text
80
443
53
```

### Packet Length
```text
Specific Sizes
```

---

## Possible Actions

### Drop
```text
Discard Traffic
```

### Rate Limit
```text
Slow Traffic
```

### Redirect
```text
Send to Scrubbing Center
```

### Mark
```text
Apply QoS Policy
```

---

## Detection

### View FlowSpec Rules
```bash
show bgp flowspec
```

---

### View BGP Information
```bash
show bgp ipv4 flowspec
```

---

## Example Rule

### Match
```text
UDP
Destination Port 53
```

### Action
```text
Drop
```

### Result
```text
DNS Flood Mitigation
```

---

## FlowSpec vs RTBH

### RTBH
```text
Drop ALL traffic
```

### FlowSpec
```text
Drop SPECIFIC traffic
```

---

## Advantages

### Granular Control
```text
Precise filtering
```

### Fast Deployment
```text
Seconds
```

### Network-Wide Distribution
```text
Via BGP
```

---

## Drawbacks

### Complexity
```text
More advanced setup
```

### Misconfiguration Risk
```text
Can block valid traffic
```

---

## Key Features
- BGP-based filtering
- DDoS mitigation
- Granular traffic control
- Dynamic rule distribution

---

## Why It Matters
- **Protects against modern attacks**
- **Faster than manual ACLs**
- **Widely used by ISPs**
- **Advanced BGP security feature**

---

## Quick Recap
**Detect → Create Rule → Advertise → Filter**
**Attack → FlowSpec → BGP → Mitigation**

---

# THANK YOU!
# ~ **V1NNN22**