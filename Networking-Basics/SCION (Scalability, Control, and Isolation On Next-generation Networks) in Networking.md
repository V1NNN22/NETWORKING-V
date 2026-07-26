# SCION (Scalability, Control, and Isolation On Next-generation Networks) in Networking
~
## Written By: VINOD N. RATHOD.
~

## What is SCION?
- **Definition:** SCION is a next-generation Internet architecture designed to provide secure, highly available, and efficient communication between networks.
- **Purpose:** It solves many security and reliability problems of today's Internet that traditional BGP cannot fix.
- **Analogy:** Think of today's Internet as a city where GPS chooses your route. With SCION, you choose exactly which roads your vehicle will travel, making the journey safer and more reliable.

---

## Why Was SCION Created?
- **Problem with Today's Internet:** BGP chooses routes automatically, giving users little control. A routing mistake or attack can affect millions of users.
- **Network Issue:** Route hijacking, Internet outages, and poor path control.
- **Solution:** SCION allows secure path selection while isolating failures so they don't spread across the Internet.

---

## The 4 Core Steps of SCION Operation

### 1. Network Discovery (Step 1)
- **Function:** Networks exchange information about available paths.
- **Role:** Builds multiple trusted communication paths.
- **Example:** ISP A learns several secure routes to ISP B.

---

### 2. Path Construction (Step 2)
- **Function:** Special Path Servers build multiple end-to-end paths.
- **Role:** Creates verified paths before communication begins.
- **Example:** Three different secure paths are generated between two countries.

---

### 3. Path Selection (Step 3)
- **Function:** The sender chooses which path to use.
- **Role:** Gives complete routing control to the sender.
- **Example:** A bank selects the safest route instead of the shortest one.

---

### 4. Secure Packet Forwarding (Step 4)
- **Function:** Packets carry their selected path inside the packet header.
- **Role:** Routers simply follow the predefined path.
- **Example:** Every router forwards the packet exactly as instructed.

---

## Components of SCION

### 1. Autonomous Systems (AS)
- Individual networks connected to the SCION architecture.
- Similar to Autonomous Systems in today's Internet.

### 2. Path Servers
- Store available communication paths.
- Help devices discover secure routes.

### 3. Beacon Servers
- Continuously discover and advertise network paths.
- Keep routing information updated.

### 4. Border Routers
- Forward packets between Autonomous Systems.
- Verify packet information before forwarding.

---

## Real-Life Example

Suppose an Indian bank communicates with its data center in Singapore.

With today's Internet:
- Traffic follows whatever BGP decides.
- A routing hijack could redirect traffic.

With SCION:
- The bank selects trusted networks only.
- Packets never travel through untrusted countries.
- If one path fails, another verified path is immediately available.

---

## Key Features
- Sender-controlled routing.
- High security.
- Built-in path verification.
- Fast recovery from failures.
- Multiple active communication paths.
- Resistant to BGP hijacking.

---

## Advantages
- Strong protection against routing attacks.
- Greater Internet reliability.
- Faster recovery during outages.
- Better privacy.
- Improved network control.

---

## Limitations
- Requires new Internet infrastructure.
- Not compatible with today's Internet by default.
- Limited global deployment.
- More complex architecture than traditional BGP.

---

## Where SCION is Used
- Government Networks
- Financial Institutions
- Research Networks
- National Critical Infrastructure
- High-Security Communications

---

## Why It Matters
- Rethinks how the Internet should work.
- Eliminates many weaknesses of BGP.
- Designed for the future Internet.
- Provides security at the architecture level instead of adding it later.

---

## Did You Know?
- Unlike today's Internet, SCION lets the sender choose the exact network path that packets will follow. This makes large-scale BGP hijacking attacks extremely difficult.

---

## Quick Recap (Mnemonic)
- **Discover → Build → Choose → Forward**
  - **Paths → Route → Control → Packet**

---

# THANK YOU!
# ~ **V1NNN22**