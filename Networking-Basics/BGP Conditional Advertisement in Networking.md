---

# BGP Conditional Advertisement in Networking  
~
## Written By: VINOD N. RATHOD.
~

## What is BGP Conditional Advertisement?

- **Definition:** BGP Conditional Advertisement is a feature that allows a router to advertise certain BGP routes only when a specified routing condition is met.
- **Purpose:** To control when backup routes or alternative advertisements are announced to BGP neighbors based on the presence or absence of other routes.
- **Analogy:** Imagine a company activating its backup delivery service only when its primary delivery service becomes unavailable. The backup is advertised when the required condition is met.

---

## The 4 Core Steps of BGP Conditional Advertisement Operation

### 1. Condition Configuration (Step 1)
- **Function:** The administrator defines the routes or prefixes that determine whether a conditional advertisement should occur.
- **Role:** Establishes the condition that controls route advertisement.
- **Examples:** A router monitors whether a specific prefix is present in its BGP table.

---

### 2. Route Monitoring (Step 2)
- **Function:** The router checks whether the configured condition is satisfied.
- **Role:** Determines whether the relevant route exists or is absent, depending on the configured policy.
- **Examples:** A router checks whether a route to its primary upstream network is still available.

---

### 3. Condition Evaluation (Step 3)
- **Function:** The router evaluates the condition against the configured advertise-map and non-exist-map or exist-map, depending on platform support.
- **Role:** Decides whether the conditional advertisement should be activated.
- **Examples:** If a monitored primary route disappears, the configured condition may become true.

---

### 4. Conditional Route Advertisement (Step 4)
- **Function:** The router advertises or withdraws the specified routes according to the evaluated condition.
- **Role:** Allows routing announcements to change automatically as network conditions change.
- **Examples:** A backup route is advertised to a neighbor when the primary route is no longer present.

---

## Key Features
- **Condition-Based Routing:** Controls advertisements using routing-table conditions.
- **Automatic Updates:** Responds to changes in monitored routes.
- **Backup Connectivity:** Can support certain primary-and-backup routing designs.
- **Policy Integration:** Uses configured route maps and supported BGP policy features.

---

## Why It Matters
- **Controlled Failover:** Helps activate backup advertisements under defined conditions.
- **Routing Flexibility:** Supports specialized advertisement policies.
- **Reduced Manual Intervention:** Allows route announcements to respond automatically to routing changes.
- **Network Resilience:** Can help maintain connectivity when the intended primary route disappears.

---

## Quick Recap (Mnemonic)
- **Configure → Monitor → Evaluate → Advertise**
  - **Define condition → Monitor routes → Evaluate policy → Advertise or withdraw routes**

---

# THANK YOU!
# ~ **V1NNN22**