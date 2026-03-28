# STP (Spanning Tree Protocol)  
~
## Written By: VINOD N. RATHOD.  
~

## What is STP?  
- **Definition:** A network protocol that prevents loops in Ethernet networks by creating a loop-free logical topology.  
- **Purpose:** Avoids broadcast storms and ensures stable Layer 2 communication in switched networks.  
- **Analogy:** Like blocking extra roads in a city to prevent traffic from endlessly looping.  

---

## The 4 Core Steps of STP Operation  

### 1. Root Bridge Election (Step 1)  
- **Function:** Switches elect a root bridge based on lowest bridge ID.  
- **Role:** Central reference point for the network topology.  
- **Examples:** Switch with lowest MAC + priority becomes root.  

---

### 2. Path Cost Calculation (Step 2)  
- **Function:** Each switch calculates shortest path to root bridge.  
- **Role:** Determines best route based on link cost.  
- **Examples:** Lower cost paths preferred.  

---

### 3. Port Role Assignment (Step 3)  
- **Function:** Ports are assigned roles like Root Port, Designated Port, or Blocked Port.  
- **Role:** Controls traffic flow and prevents loops.  
- **Examples:** One active path, others in standby/block state.  

---

### 4. Loop Prevention (Step 4)  
- **Function:** Redundant paths are blocked to avoid loops.  
- **Role:** Maintains stable and loop-free network.  
- **Examples:** Blocking alternate links until failure occurs.  

---

## Key STP Concepts  
- **Bridge ID:** Combination of priority and MAC address.  
- **Root Port:** Best path toward root bridge.  
- **Designated Port:** Forwarding port for a network segment.  
- **Blocked Port:** Disabled to prevent loops.  

---

## Why It Matters  
- **Loop Prevention:** Stops broadcast storms.  
- **Network Stability:** Ensures consistent communication.  
- **Redundancy Handling:** Keeps backup paths available.  

---

## Quick Recap (Mnemonic)  
- **Elect → Calculate → Assign → Block**  
  - **Root → Cost → Roles → Loop-Free**  

---

# THANK YOU!  
# ~ **V1NNN22**