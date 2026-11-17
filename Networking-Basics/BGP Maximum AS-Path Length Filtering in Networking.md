---

# BGP Maximum AS-Path Length Filtering in Networking  
~
## Written By: VINOD N. RATHOD.  
~

## What is BGP Maximum AS-Path Length Filtering?  
- **Definition:** BGP Maximum AS-Path Length Filtering is a routing policy that rejects or restricts BGP routes when their AS_PATH attribute exceeds a configured number of AS hops.
- **Purpose:** It helps control route acceptance, prevent unexpectedly long routing paths, and protect networks from certain routing anomalies.
- **Analogy:** Imagine a company allowing deliveries only when they pass through fewer than ten distribution centers. Routes taking too many intermediate steps are rejected.

---  

## The 4 Core Steps of AS-Path Length Filtering  

### 1. Receive BGP Route  
- **Function:** A BGP router receives a route advertisement from a neighboring autonomous system.
- **Role:** The router examines the route attributes before accepting it into the routing information base.
- **Examples:** A router receives a route for `203.0.113.0/24` with an AS_PATH containing several AS numbers.

---  

### 2. Inspect the AS_PATH Attribute  
- **Function:** The router examines the AS_PATH sequence associated with the advertised route.
- **Role:** Determines how many AS hops are represented in the path.
- **Examples:** An AS_PATH such as `65010 65020 65030` contains three AS numbers in its sequence.

---  

### 3. Compare Against the Configured Limit  
- **Function:** A routing policy compares the calculated AS-path length with the administrator-defined maximum.
- **Role:** Determines whether the route satisfies the configured path-length requirement.
- **Examples:** If the configured maximum is five and the route has seven AS hops, it fails the policy.

---  

### 4. Accept or Reject the Route  
- **Function:** The router applies the configured policy action.
- **Role:** Allows acceptable routes and rejects or otherwise handles routes exceeding the limit.
- **Examples:** A route with four AS hops is accepted, while a route with seven AS hops is rejected when the maximum is five.

---  

## Key Features  
- **AS_PATH Inspection:** Examines the BGP AS_PATH attribute.
- **Configurable Threshold:** Allows administrators to define an acceptable path length.
- **Import Policy Integration:** Can be applied when routes are received from BGP neighbors.
- **Route Filtering:** Helps restrict routes with unusually long AS paths.
- **Vendor-Dependent Configuration:** Exact commands and AS-path counting behavior can vary by platform.

---  

## Why It Matters  
- **Routing Policy Control:** Helps enforce organizational routing requirements.
- **Anomaly Detection:** Can flag unexpectedly long AS paths for further investigation.
- **Operational Protection:** May reduce acceptance of certain suspicious or undesirable advertisements.
- **Network Management:** Provides another tool for controlling external route acceptance.

**Important:** AS-path length filtering is not a complete route-security mechanism. A legitimate route can be long, and a malicious route can have a short AS_PATH. Combine it with prefix filtering, RPKI origin validation, and appropriate BGP policies.

---  

## Quick Recap (Mnemonic)  
- **Receive → Inspect → Compare → Filter**  
  - **Receive BGP route → Read AS_PATH → Check maximum length → Accept or reject**  

---  


# THANK YOU!  
# ~ **V1NNN22**