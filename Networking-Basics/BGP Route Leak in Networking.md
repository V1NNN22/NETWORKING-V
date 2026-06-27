# BGP Route Leak in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is a BGP Route Leak?  
- **Definition:** A BGP Route Leak occurs when an AS advertises routes to another AS that should not have been advertised according to routing policies.
- **Purpose (Usually Accidental):** Misconfiguration or incorrect routing policy.
- **Simple Meaning:** Sharing routes with the wrong neighbor.

---

## The 4 Core Steps of a Route Leak

### 1. Route Learning (Step 1)
- **Function:** Router learns routes from a BGP neighbor.
- **Role:** Stores them in the BGP table.

---

### 2. Policy Failure (Step 2)
- **Function:** Incorrect routing policy allows restricted routes.
- **Role:** Routes become eligible for advertisement.

---

### 3. Route Advertisement (Step 3)
- **Function:** Router advertises routes to unintended neighbors.
- **Role:** Incorrect paths spread across the Internet.

---

### 4. Traffic Diversion (Step 4)
- **Function:** Traffic follows leaked routes.
- **Result:** Congestion, outages, or suboptimal routing.

---

## Why Route Leaks Happen

### Misconfigured Filters
```text
Incorrect route policies
```

### Human Error
```text
Wrong BGP configuration
```

### Missing Prefix Filters
```text
Everything gets advertised
```

---

## Real-World Example

### ISP A
```text
Learns Google Routes
```

### Mistake
```text
Advertises them to ISP B
```

### Result
```text
Global traffic shifts unexpectedly
```

---

## Common Effects

### Congestion
```text
Unexpected traffic load
```

### Slow Internet
```text
Longer routing paths
```

### Service Outages
```text
Applications become unreachable
```

---

## Detection

### View Advertised Routes
```bash
show ip bgp neighbors advertised-routes
```

---

### Check BGP Table
```bash
show ip bgp
```

---

### Validate Policies
```bash
show route-map
```

---

## Prevention

### Prefix Filtering
```text
Advertise only allowed prefixes
```

### Route Maps
```text
Control advertisements
```

### RPKI
```text
Validate route origins
```

### Peer Lock
```text
Prevent accidental leaks
```

---

## Route Leak vs Route Hijacking

### Route Leak
```text
Valid route shared incorrectly
```

### Route Hijacking
```text
Fake route advertised intentionally
```

---

## Key Features
- Usually accidental
- Policy violation
- Can affect the global Internet
- Difficult to troubleshoot

---

## Why It Matters
- **Causes Internet outages**
- **Disrupts traffic flow**
- **Highlights importance of routing policies**
- **Major concern for ISPs**

---

## Quick Recap
**Learn → Misconfigure → Advertise → Divert**
**Valid Route → Wrong Neighbor → Traffic Shift → Problem**

---

# THANK YOU!
# ~ **V1NNN22**