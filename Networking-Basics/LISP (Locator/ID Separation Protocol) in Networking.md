# LISP (Locator/ID Separation Protocol) in Networking
~
## Written By: VINOD N. RATHOD.
~

## What is LISP?
- **Definition:** LISP (Locator/ID Separation Protocol) is a networking architecture that separates a device's identity from its current network location.
- **Purpose:** Allows an endpoint to keep the same identity while its traffic can be routed through different network locations.
- **Analogy:** Your phone number identifies you, while your physical address tells people where you are. If you move houses, your identity stays the same but your location changes. LISP applies a similar idea to IP networking.

---

## Why Was LISP Created?
- **Problem with Traditional IP:** An IP address performs two jobs: identifying an endpoint and indicating where that endpoint is located in the network.
- **Network Issue:** This becomes difficult when devices move, networks become highly distributed, or organizations need scalable routing.
- **Solution:** LISP separates the endpoint's identity from the routing location.

---

## The 4 Core Steps of LISP Operation

### 1. Endpoint Identification (Step 1)
- **Function:** A device is assigned an Endpoint Identifier (EID).
- **Role:** Identifies the endpoint independently of its physical network location.
- **Example:** A virtual machine keeps the same EID even after moving to another data center.

---

### 2. Locator Discovery (Step 2)
- **Function:** The network determines the current Routing Locator (RLOC) associated with the endpoint.
- **Role:** Identifies where the endpoint is currently reachable.
- **Example:** EID `10.10.10.10` is currently reachable through RLOC `192.0.2.1`.

---

### 3. Mapping Lookup (Step 3)
- **Function:** A LISP router queries the mapping system to find the RLOC associated with the destination EID.
- **Role:** Converts "who am I trying to reach?" into "where should I send the packet?"
- **Example:** Router A asks the mapping system where EID `10.10.10.10` is currently located.

---

### 4. Packet Encapsulation and Forwarding (Step 4)
- **Function:** The packet is encapsulated with a LISP header and sent toward the destination RLOC.
- **Role:** Allows normal IP routing to transport the packet through the network.
- **Example:** The original packet is carried inside a LISP tunnel toward the destination site.

---

## Components of LISP

### 1. EID (Endpoint Identifier)
- Identifies an endpoint.
- Represents the "who" in LISP.

### 2. RLOC (Routing Locator)
- Identifies where an endpoint is reachable.
- Represents the "where" in LISP.

### 3. ITR (Ingress Tunnel Router)
- Receives packets from an endpoint.
- Looks up the destination EID.
- Encapsulates the packet toward the appropriate RLOC.

### 4. ETR (Egress Tunnel Router)
- Receives the encapsulated LISP packet.
- Removes the LISP encapsulation.
- Delivers the original packet to the destination endpoint.

### 5. Map-Server
- Receives EID-to-RLOC registrations.
- Maintains mapping information.

### 6. Map-Resolver
- Helps an ITR discover the RLOC associated with a destination EID.

---

## Real-Life Example

Suppose a company has a virtual machine:

**EID:** `10.10.10.10`

Today it is running in:

**Data Center A → RLOC:** `192.0.2.1`

Later, the VM moves to:

**Data Center B → RLOC:** `198.51.100.1`

With traditional location-dependent addressing, moving the VM can create routing complications.

With LISP:

- The EID remains `10.10.10.10`.
- The RLOC changes.
- The mapping system updates the relationship.
- Traffic is automatically sent to the new location.

---

## Key Features
- **Identity/Location Separation:** Separates endpoint identity from network location.
- **Overlay Networking:** Creates an overlay over an existing IP network.
- **Dynamic Mapping:** EIDs can map to changing RLOCs.
- **Traffic Engineering:** Multiple RLOCs can provide different forwarding choices.
- **Mobility Support:** Useful when endpoints move between network locations.

---

## Advantages
- Reduces the need to advertise every endpoint into the core routing table.
- Supports mobility and multihoming.
- Enables scalable network virtualization.
- Allows multiple routing locators for an endpoint.
- Provides additional control over traffic paths.

---

## Limitations
- Requires LISP-capable infrastructure.
- Introduces additional encapsulation overhead.
- Requires a mapping system.
- Adds architectural complexity.
- Not universally deployed across the public Internet.

---

## Where LISP is Used
- Data Center Overlays
- Enterprise WANs
- Network Virtualization
- Mobility Networks
- Software Defined Networking (SDN)
- Multi-Homed Networks

---

## Why It Matters
- Challenges the traditional assumption that an IP address must represent both identity and location.
- Provides a scalable approach to endpoint mobility and multihoming.
- Helps reduce routing-table growth by separating endpoint information from core routing information.
- Influenced the design of modern overlay and locator/identifier separation architectures.

---

## Did You Know?
- LISP's central idea is extremely simple: **EID answers "who?" while RLOC answers "where?"**
- This separation allows an endpoint to move without necessarily changing its identity.

---

## Quick Recap (Mnemonic)
- **Identify → Locate → Map → Encapsulate**
  - **EID → RLOC → Mapping → Tunnel**

---

# THANK YOU!
# ~ **V1NNN22**