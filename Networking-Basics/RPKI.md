# RPKI (Resource Public Key Infrastructure) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is RPKI?  
- **Definition:** RPKI is a security framework that verifies whether an Autonomous System (AS) is authorized to advertise a specific IP prefix.
- **Purpose:** Prevent BGP route hijacking and route leaks.
- **Simple Meaning:** A digital certificate that proves, "Yes, this AS really owns this IP prefix."

---

## The 4 Core Steps of RPKI

### 1. ROA Creation (Step 1)
- **Function:** IP prefix owner creates a Route Origin Authorization (ROA).
- **Role:** Specifies which AS can advertise the prefix.

---

### 2. ROA Publication (Step 2)
- **Function:** ROA is published in the RPKI repository.
- **Role:** Makes authorization publicly available.

---

### 3. Route Validation (Step 3)
- **Function:** Routers compare BGP routes with ROAs.
- **Role:** Verify route legitimacy.

---

### 4. Routing Decision (Step 4)
- **Function:** Router accepts or rejects the route.
- **Result:** Invalid advertisements are filtered.

---

## Why RPKI Exists

### Prevent
```text
BGP Route Hijacking
```

### Prevent
```text
Accidental Route Leaks
```

### Improve
```text
Internet Routing Security
```

---

## Route Validation States

### Valid
```text
Correct AS advertises prefix
```

### Invalid
```text
Unauthorized AS advertises prefix
```

### Not Found
```text
No ROA exists
```

---

## Real-World Example

### Prefix
```text
192.0.2.0/24
```

### Authorized AS
```text
AS65001
```

### Advertisement
```text
AS65055
```

### Result
```text
Route = Invalid
```

---

## Detection

### Check Validation Status
```bash
show bgp rpki
```

---

### View RPKI Routes
```bash
show ip bgp
```

Look for:
```text
Valid
Invalid
NotFound
```

---

## Components

### ROA
```text
Route Origin Authorization
```

### Validator
```text
Checks ROAs
```

### Router
```text
Applies validation
```

---

## Benefits

### Security
```text
Stops fake route advertisements
```

### Stability
```text
Reduces routing incidents
```

### Trust
```text
Verifies route ownership
```

---

## Limitations

### Only Validates
```text
Route Origin
```

### Does NOT Validate
```text
Entire AS Path
```

---

## RPKI vs Traditional BGP

### Traditional BGP
```text
Trust everyone
```

### RPKI
```text
Verify before trusting
```

---

## Key Features
- Cryptographic validation
- Prevents route hijacking
- Uses digital certificates
- Improves BGP security

---

## Why It Matters
- **Secures Internet routing**
- **Protects IP prefixes**
- **Reduces global outages**
- **Essential for modern ISPs**

---

## Quick Recap
**Create ROA → Publish → Validate → Accept/Reject**
**Certificate → Verification → Decision → Secure Routing**

---

# THANK YOU!
# ~ **V1NNN22**