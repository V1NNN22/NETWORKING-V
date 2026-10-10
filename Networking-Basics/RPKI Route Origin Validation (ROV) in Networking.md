---

# RPKI Route Origin Validation (ROV) in Networking  
~
## Written By: VINOD N. RATHOD.
~

## What is RPKI Route Origin Validation (ROV)?

- **Definition:** RPKI Route Origin Validation (ROV) is a BGP security mechanism that uses Resource Public Key Infrastructure (RPKI) data to check whether an autonomous system is authorized to originate a particular IP prefix.
- **Purpose:** To help detect and reject invalid BGP route announcements that may result from accidental misconfiguration or certain prefix hijacking attempts.
- **Analogy:** Imagine an airport checking whether an airline is authorized to operate a particular flight route. If the authorization does not match, the flight is flagged for review.

---

## The 4 Core Steps of RPKI Route Origin Validation Operation

### 1. Route Authorization Creation (Step 1)
- **Function:** An IP address resource holder creates a Route Origin Authorization (ROA) specifying an IP prefix, an authorized origin AS, and an optional maximum prefix length.
- **Role:** Establishes which autonomous system is authorized to originate the specified prefix.
- **Examples:** A ROA authorizes AS 64500 to originate `203.0.113.0/24`.

---

### 2. RPKI Data Retrieval (Step 2)
- **Function:** A relying party retrieves and validates RPKI data, producing validated records that routers can access through a supported RPKI-to-router protocol.
- **Role:** Makes authenticated prefix-origin authorization data available to routing infrastructure.
- **Examples:** A router receives validated prefix authorization data from an RPKI cache server.

---

### 3. BGP Route Origin Validation (Step 3)
- **Function:** The router compares a received BGP route's prefix and origin AS against the available validated ROA data.
- **Role:** Classifies the route as **Valid**, **Invalid**, or **NotFound**.
- **Examples:**
  - **Valid:** The prefix and origin AS match an authorization.
  - **Invalid:** An authorization exists, but the origin AS or prefix length violates it.
  - **NotFound:** No covering authorization is available.

---

### 4. Routing Policy Enforcement (Step 4)
- **Function:** The network operator applies routing policy based on the validation state.
- **Role:** Helps prevent routes with invalid origin authorizations from being selected or propagated.
- **Examples:** A router rejects an Invalid route while continuing to consider Valid and NotFound routes according to its configured policy.

---

## Key Features
- **Cryptographic Authorization:** Uses RPKI data to establish authorized prefix origins.
- **Three Validation States:** Classifies routes as Valid, Invalid, or NotFound.
- **BGP Integration:** Allows operators to incorporate validation results into routing policies.
- **Hijack Mitigation:** Helps detect and mitigate unauthorized route-origin announcements.

---

## Why It Matters
- **Improved Routing Security:** Helps identify suspicious BGP announcements.
- **Reduced Hijacking Risk:** Can prevent acceptance of routes that conflict with valid origin authorizations.
- **Misconfiguration Detection:** Identifies certain mistakes involving origin AS numbers and prefix lengths.
- **Internet Resilience:** Supports more trustworthy interdomain routing when deployed consistently.

---

## Quick Recap (Mnemonic)
- **Authorize → Retrieve → Validate → Enforce**
  - **Create ROA → Retrieve validated data → Check BGP origin → Apply routing policy**

---

# THANK YOU!
# ~ **V1NNN22**