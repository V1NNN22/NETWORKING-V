---

# BGP Deterministic MED in Networking  
~
## Written By: VINOD N. RATHOD.  
~

## What is BGP Deterministic MED?  
- **Definition:** BGP Deterministic MED is a route-selection behavior that ensures BGP compares Multi-Exit Discriminator (MED) values consistently among routes received from the same neighboring Autonomous System (AS).
- **Purpose:** It removes dependence on the order in which routes are received when comparing MED values.
- **Analogy:** Imagine a competition where contestants from each team are compared using their team's best score first. The result stays consistent regardless of the order in which contestants arrive.

---  

## The 4 Core Steps of Deterministic MED Operation  

### 1. Receive BGP Routes  
- **Function:** A BGP router receives multiple candidate routes to the same destination from different peers.
- **Role:** These routes enter the BGP decision process.
- **Examples:** A router receives three routes to `203.0.113.0/24` from different neighboring ASes.

---  

### 2. Group Routes by Neighboring AS  
- **Function:** The router groups routes based on the neighboring AS from which they were received.
- **Role:** MED comparisons are performed within the relevant neighboring-AS groups.
- **Examples:** Routes received from AS 65010 are compared with one another before comparing against routes from AS 65020.

---  

### 3. Compare MED Values Consistently  
- **Function:** Within each neighboring-AS group, BGP compares MED values and determines the preferred route.
- **Role:** Ensures that route evaluation does not depend on the order in which routes entered the router.
- **Examples:** Among routes from AS 65010 with MED values of 100, 50, and 200, the route with MED 50 is preferred in the MED comparison.

---  

### 4. Continue the BGP Decision Process  
- **Function:** The router compares the resulting candidate routes using the remaining BGP best-path rules.
- **Role:** MED is only one factor in the complete BGP route-selection process.
- **Examples:** A route with a lower MED may still lose due to higher-priority BGP attributes such as LOCAL_PREF.

---  

## Key Features  
- **Consistent MED Comparison:** Reduces route-selection differences caused by route arrival order.
- **AS-Based Grouping:** Compares MED values among routes from the same neighboring AS.
- **BGP Decision Process Integration:** Works as part of the overall best-path selection process.
- **Configuration-Based Behavior:** Requires platform support and appropriate configuration.
- **Lower MED Preference:** A lower MED is preferred when MED is compared.

---  

## Why It Matters  
- **Predictable Routing:** Helps make BGP route selection more consistent.
- **Reduces Route Oscillation Risk:** Can prevent certain order-dependent MED comparison problems.
- **Improves Troubleshooting:** Makes route-selection behavior easier to analyze.
- **Better Multi-Homed Networks:** Useful when an AS receives multiple routes from the same external AS.

---  

## Quick Recap (Mnemonic)  
- **Receive → Group → Compare → Select**  
  - **Collect BGP routes → Group by neighboring AS → Compare MED values → Continue best-path selection**  

---  


# THANK YOU!  
# ~ **V1NNN22**