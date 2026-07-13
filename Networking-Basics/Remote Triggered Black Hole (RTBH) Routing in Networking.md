# Remote Triggered Black Hole (RTBH) Routing in Networking
~
## Written By: VINOD N. RATHOD.
~

## What is Remote Triggered Black Hole (RTBH) Routing?
- **Definition:** A security technique that uses BGP to immediately discard unwanted or malicious traffic before it reaches the target network.
- **Purpose:** Protects networks from large-scale attacks such as Distributed Denial of Service (DDoS).
- **Analogy:** Like closing a highway exit before thousands of unwanted vehicles reach your city. The traffic is stopped far away instead of causing congestion inside.

---

## The 4 Core Steps of RTBH Operation

### 1. Attack Detection (Step 1)
- **Function:** The network identifies suspicious or attack traffic.
- **Role:** Determines the target IP address.
- **Examples:** DDoS attack detected against a web server.

---

### 2. Blackhole Route Creation (Step 2)
- **Function:** A special BGP route with a predefined community is advertised.
- **Role:** Signals routers to discard traffic for the target.
- **Examples:** Route tagged with a "blackhole" community.

---

### 3. Traffic Discarding (Step 3)
- **Function:** Routers match the blackhole route and drop incoming packets.
- **Role:** Prevents attack traffic from entering the network.
- **Examples:** ISP edge routers silently discard malicious packets.

---

### 4. Normal Routing Restoration (Step 4)
- **Function:** The blackhole route is removed after the attack ends.
- **Role:** Restores normal traffic flow.
- **Examples:** Legitimate users regain access to the server.

---

## Key Features
- **Fast DDoS Mitigation:** Blocks attacks within seconds.
- **BGP-Based:** Uses existing BGP infrastructure.
- **Scalable:** Effective across ISP and enterprise networks.
- **Low Resource Usage:** Stops malicious traffic before it consumes bandwidth.

---

## Why It Matters
- **Improves Availability:** Keeps the rest of the network operational.
- **Protects Critical Services:** Reduces the impact of DDoS attacks.
- **Simple Deployment:** Requires minimal changes to existing BGP networks.

---

## Quick Recap (Mnemonic)
- **Detect → Advertise → Drop → Restore**
  - **Attack → BGP → Traffic → Network**

---

# THANK YOU!
# ~ **V1NNN22**