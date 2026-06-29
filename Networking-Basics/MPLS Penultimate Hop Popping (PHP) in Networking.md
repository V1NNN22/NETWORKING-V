# MPLS Penultimate Hop Popping (PHP) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is Penultimate Hop Popping (PHP)?  
- **Definition:** Penultimate Hop Popping (PHP) is an MPLS optimization where the second-to-last router removes the MPLS label before forwarding the packet to the last router.
- **Purpose:** Reduce processing load on the egress router.
- **Simple Meaning:** The router before the destination removes the label so the destination router doesn't have to.

---

## The 4 Core Steps of PHP

### 1. Label Assignment (Step 1)
- **Function:** Ingress router pushes an MPLS label.
- **Role:** Establish MPLS forwarding path.

---

### 2. Label Switching (Step 2)
- **Function:** Intermediate routers swap labels.
- **Role:** Forward packet through MPLS network.

---

### 3. Label Popping (Step 3)
- **Function:** Penultimate router removes the MPLS label.
- **Role:** Sends a normal IP packet to the egress router.

---

### 4. Final Forwarding (Step 4)
- **Function:** Egress router performs only IP lookup.
- **Result:** Faster packet forwarding.

---

## Why PHP Exists

### Reduce
```text
Egress Router Load
```

### Improve
```text
Forwarding Efficiency
```

### Optimize
```text
MPLS Performance
```

---

## Real-World Example

### Packet Path
```text
R1 → R2 → R3 → R4
```

### MPLS Label
```text
100
```

### PHP Action
```text
R3 removes Label 100
```

### Result
```text
R4 receives plain IP packet
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

### Penultimate Router
```text
Pop Label
```

↓

### Egress
```text
Forward IP Packet
```

---

## Detection

### View MPLS Table
```bash
show mpls forwarding-table
```

---

### View LFIB
```bash
show mpls forwarding-table detail
```

Look for:
```text
Pop Label
```

---

## Configuration

### Cisco MPLS
```bash
mpls ip
```

(PHP is enabled automatically in most MPLS deployments.)

---

## Advantages

### Faster Processing
```text
Less work for egress router
```

### Better Scalability
```text
Improved MPLS performance
```

### Lower CPU Usage
```text
Reduced label operations
```

---

## Drawbacks

### Less Label Visibility
```text
Egress cannot inspect label
```

### Not Ideal For
```text
Some VPN/QoS scenarios
```

---

## PHP vs UHP

### PHP
```text
Second-last router removes label
```

### UHP (Ultimate Hop Popping)
```text
Last router removes label
```

---

## Key Features
- MPLS optimization
- Automatic in most networks
- Reduces egress processing
- Improves forwarding efficiency

---

## Why It Matters
- **Speeds up MPLS forwarding**
- **Improves scalability**
- **Reduces router workload**
- **Core MPLS concept**

---

## Quick Recap
**Push → Swap → Pop → Forward**
**Ingress → Core → Penultimate → Egress**

---

# THANK YOU!
# ~ **V1NNN22**