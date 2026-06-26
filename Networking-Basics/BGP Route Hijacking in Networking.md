# BGP Route Hijacking in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is BGP Route Hijacking?  
- **Definition:** BGP Route Hijacking occurs when an Autonomous System (AS) falsely advertises IP prefixes that it does not own.
- **Purpose (Attacker):** Redirect, intercept, or disrupt Internet traffic.
- **Simple Meaning:** Someone falsely claims ownership of another network's IP addresses.

---

## The 4 Core Steps of BGP Route Hijacking

### 1. Fake Advertisement (Step 1)
- **Function:** Attacker announces someone else's IP prefix.
- **Role:** Creates a fraudulent BGP route.

---

### 2. Route Propagation (Step 2)
- **Function:** Neighboring ASes accept and propagate the fake route.
- **Role:** Spreads the incorrect information.

---

### 3. Traffic Redirection (Step 3)
- **Function:** Internet routers select the fake path.
- **Role:** Traffic flows toward the attacker.

---

### 4. Attack Outcome (Step 4)
- **Function:** Attacker drops, inspects, or forwards traffic.
- **Result:** Service disruption or interception.

---

## Why Route Hijacking Happens

### Traffic Interception
```text
Spy on communications
```

### DDoS
```text
Disrupt services
```

### Misconfiguration
```text
Accidental advertisements
```

---

## Real-World Example

### Legitimate Route
```text
203.0.113.0/24 → AS65001
```

### Fake Route
```text
203.0.113.0/24 → AS65099
```

### Result
```text
Traffic follows attacker
```

---

## Types of Hijacking

### Exact Prefix
```text
Same IP prefix
```

### More Specific Prefix
```text
203.0.113.0/25
```

### Result
```text
More specific route usually wins
```

---

## Detection

### View BGP Table
```bash
show ip bgp
```

---

### Check Route Origin
```bash
show ip bgp 203.0.113.0
```

---

### Validate Using RPKI
```bash
show bgp rpki
```

---

## Prevention

### RPKI
```text
Validate Route Origin
```

### Prefix Filtering
```text
Accept trusted prefixes only
```

### IRR Filtering
```text
Verify route ownership
```

---

## Consequences

### Traffic Loss
```text
Blackhole
```

### Data Theft
```text
Traffic interception
```

### Outages
```text
Service unavailable
```

---

## Route Hijacking vs Route Leak

### Route Hijacking
```text
Unauthorized advertisement
```

### Route Leak
```text
Valid route shared incorrectly
```

---

## Key Features
- Targets BGP
- Redirects Internet traffic
- Can be accidental or malicious
- Global impact possible

---

## Why It Matters
- **Threatens Internet security**
- **Can cause worldwide outages**
- **Motivated adoption of RPKI**
- **Critical BGP attack technique**

---

## Quick Recap
**Advertise → Propagate → Redirect → Exploit**
**Fake Prefix → BGP Update → Wrong Path → Attack**

---

# THANK YOU!
# ~ **V1NNN22**