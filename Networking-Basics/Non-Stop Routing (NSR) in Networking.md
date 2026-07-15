# Non-Stop Routing (NSR) in Networking
~
## Written By: VINOD N. RATHOD.
~

## What is Non-Stop Routing (NSR)?
- **Definition:** A high-availability feature that allows a router to continue routing traffic even if its routing process fails or restarts.
- **Purpose:** Eliminates routing interruptions by synchronizing routing information between redundant control planes.
- **Analogy:** Like having two pilots flying the same aircraft. If one pilot suddenly becomes unavailable, the other immediately takes control without affecting the flight.

---

## The 4 Core Steps of Non-Stop Routing Operation

### 1. State Synchronization (Step 1)
- **Function:** The active routing engine continuously synchronizes routing information with the standby engine.
- **Role:** Keeps both control planes identical.
- **Examples:** Routing tables and protocol states are copied in real time.

---

### 2. Failure Detection (Step 2)
- **Function:** The active routing engine fails or restarts.
- **Role:** Triggers an immediate switchover.
- **Examples:** Software crash or routing daemon restart.

---

### 3. Instant Switchover (Step 3)
- **Function:** The standby routing engine becomes active.
- **Role:** Continues routing without rebuilding neighbor relationships.
- **Examples:** BGP and OSPF sessions remain active.

---

### 4. Continuous Forwarding (Step 4)
- **Function:** Traffic keeps flowing while synchronization resumes.
- **Role:** Prevents packet loss and routing convergence delays.
- **Examples:** Users experience little to no network interruption.

---

## Key Features
- **Zero Routing Downtime:** Maintains uninterrupted routing.
- **High Availability:** Designed for mission-critical networks.
- **Fast Recovery:** No routing protocol reconvergence.
- **Protocol Support:** Commonly used with BGP, OSPF, and IS-IS.

---

## Why It Matters
- **Maximum Uptime:** Keeps services running during failures.
- **Improved Reliability:** Critical for ISPs and data centers.
- **Better User Experience:** Minimizes packet loss and service disruption.

---

## Quick Recap (Mnemonic)
- **Sync → Detect → Switch → Continue**
  - **State → Failure → Standby → Traffic**

---

# THANK YOU!
# ~ **V1NNN22**