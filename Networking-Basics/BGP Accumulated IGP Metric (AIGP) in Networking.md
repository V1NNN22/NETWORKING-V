---

# BGP Accumulated IGP Metric (AIGP) in Networking  
~
## Written By: VINOD N. RATHOD.  
~

## What is BGP AIGP?  
- **Definition:** The Accumulated IGP Metric (AIGP) is a BGP path attribute that carries an accumulated metric representing the cost of reaching a destination through an interior network.
- **Purpose:** It helps BGP routers compare routes across multiple ASes that belong to a coordinated routing domain, using IGP cost information.
- **Analogy:** Imagine choosing a delivery route across several connected warehouses. Instead of looking only at the next warehouse, you consider the total road cost accumulated along the journey.

---  

## The 4 Core Steps of AIGP Operation  

### 1. IGP Metric Calculation  
- **Function:** Routers calculate internal path costs using an Interior Gateway Protocol (IGP), such as OSPF or IS-IS.
- **Role:** These costs represent the internal distance to reach a BGP next hop or destination.
- **Examples:** A router may calculate an IGP cost of 20 to reach the next-hop router.

---  

### 2. AIGP Attribute Assignment  
- **Function:** AIGP information is attached to a BGP route when it is advertised within a network configured to use AIGP.
- **Role:** It provides a metric that can be accumulated as the route passes through participating BGP speakers.
- **Examples:** A route may carry an AIGP metric of 20 when it enters a BGP domain.

---  

### 3. Metric Accumulation  
- **Function:** Participating BGP routers add relevant IGP costs to the AIGP metric as the route is propagated.
- **Role:** This allows the accumulated metric to represent more than just the local router's IGP distance.
- **Examples:** A route with an AIGP value of 20 may be advertised onward with a value of 35 after an additional cost of 15 is added.

---  

### 4. BGP Route Comparison  
- **Function:** BGP uses AIGP information during route selection when the attribute is enabled and applicable.
- **Role:** It helps select a route with a lower accumulated metric, subject to BGP's decision process and configuration.
- **Examples:** Between two otherwise comparable routes, a router may prefer an AIGP metric of 35 over 50.

---  

## Key Features  
- **Metric Accumulation:** Carries an accumulated cost across participating BGP speakers.
- **IGP-Aware Selection:** Allows BGP route selection to consider internal network cost.
- **Coordinated Deployment:** Intended for networks with an agreed metric domain and compatible configuration.
- **Route Attribute:** AIGP is carried as a BGP path attribute.
- **Policy Sensitive:** AIGP behavior depends on configuration and where the attribute is added, propagated, or removed.

---  

## Why It Matters  
- **Better Path Selection:** Can help choose routes with lower end-to-end internal cost.
- **Multi-AS Coordination:** Useful when multiple autonomous systems operate as one coordinated routing environment.
- **Traffic Engineering:** Supports routing decisions based on accumulated internal metrics.
- **Avoids Local-Only Decisions:** Helps BGP compare paths using metric information beyond a single router's local IGP cost.

---  

## Quick Recap (Mnemonic)  
- **Calculate → Attach → Accumulate → Compare**  
  - **Find IGP cost → Add AIGP → Carry the growing metric → Prefer lower cost when applicable**  

---  


# THANK YOU!  
# ~ **V1NNN22**