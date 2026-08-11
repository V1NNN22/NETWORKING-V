# BGP-LS (BGP Link-State) in Networking
~
## Written By: VINOD N. RATHOD.
~

## What is BGP-LS?
- **Definition:** BGP-LS (BGP Link-State) is a BGP extension used to distribute detailed network topology information, such as routers, links, metrics, and network attributes, to external controllers and applications.
- **Purpose:** Provides a centralized system with a detailed view of the network topology without requiring the controller to participate directly in every IGP.
- **Analogy:** Imagine every city's traffic department maintaining its own road map. BGP-LS collects those maps and sends them to a central traffic-control center so it can see the entire highway system.

---

## Why Was BGP-LS Created?
- **Problem with Traditional Routing:** OSPF and IS-IS know the network topology, but external controllers and applications cannot easily consume that information.
- **Network Issue:** SDN controllers, Path Computation Elements (PCEs), and traffic-engineering applications need detailed topology information.
- **Solution:** BGP-LS carries link-state information from the routing domain to those external systems.

---

## The 4 Core Steps of BGP-LS Operation

### 1. Topology Discovery (Step 1)
- **Function:** OSPF or IS-IS discovers routers, links, and network information.
- **Role:** Builds the original link-state database.
- **Example:** IS-IS learns that Router A connects to Router B through a 10-Gbps link.

---

### 2. Topology Collection (Step 2)
- **Function:** A BGP-LS speaker learns the topology information from the IGP.
- **Role:** Converts the internal link-state information into information that can be advertised through BGP.
- **Example:** A router learns the network topology from IS-IS and prepares it for BGP-LS advertisement.

---

### 3. BGP-LS Advertisement (Step 3)
- **Function:** BGP-LS advertises topology information to a controller or other BGP-LS peer.
- **Role:** Transfers detailed network information outside the normal IGP domain.
- **Example:** Router A sends information about Router B, its links, metrics, and capabilities to a Path Computation Element.

---

### 4. Topology Analysis (Step 4)
- **Function:** The receiving controller analyzes the topology information.
- **Role:** Calculates paths, performs traffic engineering, or makes network optimization decisions.
- **Example:** A controller determines the best path for a high-priority traffic flow.

---

## Components of BGP-LS

### 1. IGP
- Usually OSPF or IS-IS.
- Discovers the actual network topology.

### 2. BGP-LS Speaker
- Receives topology information from the IGP.
- Advertises that information using BGP-LS.

### 3. BGP-LS Peer
- Receives topology information.
- Can be a controller, PCE, or another network system.

### 4. PCE (Path Computation Element)
- Uses topology information to calculate optimized paths.
- Can support advanced traffic engineering.

### 5. Link-State Database
- Contains information about routers, links, metrics, and other topology attributes.

---

## What Information Can BGP-LS Carry?

- **Node Information:** Router IDs and capabilities.
- **Link Information:** Connected routers and link attributes.
- **Prefix Information:** Networks associated with routers.
- **Link Metrics:** Cost or metric of links.
- **Traffic Engineering Information:** Bandwidth and other TE attributes.
- **Segment Routing Information:** Segment IDs and related attributes.

---

## Real-Life Example

Suppose an ISP has:

Router A → Router B → Router D
       ↘ Router C ↗

The ISP's IS-IS network already knows:

- Which routers exist.
- Which links connect them.
- Link costs.
- Available topology information.

A centralized PCE needs this information to calculate optimized paths.

Instead of building a separate topology-discovery mechanism:

IS-IS
↓
BGP-LS Speaker
↓
BGP-LS
↓
PCE / Controller
↓
Path Computation

The controller now has a detailed view of the network.

---

## Key Features
- **Topology Distribution:** Shares detailed network topology.
- **IGP Integration:** Works with OSPF and IS-IS.
- **Controller Friendly:** Designed for external network applications.
- **Traffic Engineering:** Provides information required for path computation.
- **Segment Routing Support:** Can distribute SR-related topology information.

---

## Advantages
- Gives controllers a detailed network view.
- Avoids requiring controllers to participate directly in the IGP.
- Supports centralized path computation.
- Enables advanced traffic engineering.
- Works well with Segment Routing and SDN architectures.

---

## Limitations
- Requires BGP-LS support.
- Adds another control-plane component.
- Does not itself calculate or install the optimal path.
- Depends on the underlying IGP for topology discovery.
- Requires careful synchronization between topology sources and consumers.

---

## Where BGP-LS is Used
- ISP Core Networks
- Segment Routing Networks
- SDN Controllers
- Path Computation Elements (PCE)
- Traffic Engineering Systems
- 5G Transport Networks
- Large Enterprise Backbones

---

## Why It Matters
- Connects traditional distributed routing with centralized network intelligence.
- Gives controllers a real-time topology view.
- Enables advanced traffic engineering.
- Plays an important role in Segment Routing architectures.
- Allows BGP to act as a topology-information distribution mechanism.

---

## Did You Know?
- **BGP-LS does not replace OSPF or IS-IS.**
- OSPF/IS-IS still discover the topology.
- BGP-LS simply carries that topology information to systems that need to understand the network from a broader perspective.

---

## Quick Recap (Mnemonic)
- **Discover → Collect → Advertise → Compute**
  - **IGP → BGP-LS Speaker → Controller → Path**

---

# THANK YOU!
# ~ **V1NNN22**