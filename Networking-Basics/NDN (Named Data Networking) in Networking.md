# NDN (Named Data Networking) in Networking
~
## Written By: VINOD N. RATHOD.
~

## What is NDN?
- **Definition:** NDN (Named Data Networking) is an information-centric networking architecture where packets request data by its name rather than addressing a specific host using an IP address.
- **Purpose:** Focuses networking on **what data is needed** instead of **which machine should provide it**.
- **Analogy:** Traditional IP networking is like saying, "Go to Apartment 302 and ask for the movie." NDN is like saying, "I need this movie." The network finds a valid source that has it. Humans finally taught packets to care about content instead of apartments.

---

## The 4 Core Steps of NDN Operation

### 1. Data Naming (Step 1)
- **Function:** Content is identified using a hierarchical name.
- **Role:** Provides a unique way to describe the requested data.
- **Examples:** `/movies/movie1/video/segment01` identifies a particular piece of content.

---

### 2. Interest Packet (Step 2)
- **Function:** A consumer sends an Interest packet containing the name of the requested data.
- **Role:** Tells the network what content is required.
- **Examples:** A user requests `/news/today/article1`.

---

### 3. Data Retrieval (Step 3)
- **Function:** An NDN router forwards the Interest toward a location that can provide the requested content.
- **Role:** Allows the data to come from an original server, cache, or another available source.
- **Examples:** A nearby router already has the requested video segment cached and can return it directly.

---

### 4. Data Return and Caching (Step 4)
- **Function:** The requested Data packet travels back toward the consumer.
- **Role:** Routers can cache the data for future requests.
- **Examples:** If another user requests the same video segment, a nearby router can respond from its cache instead of contacting the original server.

---

## Key Components

### 1. Interest Packet
- Requests specific content.
- Contains the name of the desired data.

### 2. Data Packet
- Carries the requested content.
- Contains the data name and security information.

### 3. Content Store
- Stores previously retrieved data.
- Allows routers to satisfy future requests from their cache.

### 4. Pending Interest Table (PIT)
- Tracks outstanding Interest requests.
- Records where requested content needs to be forwarded.

### 5. Forwarding Information Base (FIB)
- Contains information about where Interests should be forwarded.
- Uses content-name prefixes rather than traditional IP destinations.

---

## Real-Life Example

Suppose 1,000 users in a city request the same video:

```text
             Original Content
                    |
                    |
              NDN Network
             /     |     \
            /      |      \
        Router A Router B Router C
           |        |        |
        Users     Users     Users

Traditional IP Networking:

Users communicate with the content server.

Large amounts of traffic may travel repeatedly toward the same server.


NDN:

The first request retrieves the content.

Routers can cache the Data packet.

Later users can retrieve the same content from nearby caches.



---

Key Features

Content-Based Addressing: Requests data by name.

In-Network Caching: Routers can temporarily store content.

Multi-Source Retrieval: Data can come from multiple valid sources.

Data-Centric Security: Security can be associated with the data itself.

Interest/Data Model: Consumers request named content using Interest packets.

Location Independence: Content does not need to remain tied to one server location.



---

Advantages

Reduces duplicate traffic.

Improves content delivery efficiency.

Supports distributed caching.

Can handle content mobility more naturally.

Allows data to be retrieved from multiple sources.

Makes the network more content-aware.



---

Limitations

Requires a major architectural change from traditional IP networking.

Routing large numbers of content names can be challenging.

Existing applications and infrastructure are primarily IP-based.

PIT state can become significant under heavy traffic.

Large-scale deployment requires ecosystem-wide adoption.



---

Where NDN is Used

Content Distribution

Information-Centric Networking Research

IoT Networks

Vehicular Networks

Edge Computing

Distributed Systems

Future Internet Research



---

Why It Matters

Content Focus: Changes networking from host-to-host communication to data retrieval.

Caching: Allows routers to satisfy repeated requests locally.

Mobility: Separates content identity from physical server location.

Efficiency: Can reduce unnecessary long-distance traffic.

Future Internet: Explores an alternative architecture to traditional IP networking.



---

NDN vs Traditional IP Networking

Feature	Traditional IP	NDN

Main Identity	Host/IP Address	Data Name
Communication	Host-to-Host	Consumer-to-Data
Routing	IP Prefixes	Content Names
Caching	Usually External	Built Into Architecture
Data Source	Specific Host	Any Valid Source
Security	Often Connection/Channel Focused	Data-Centric
Mobility	More Complicated	More Naturally Supported



---

Did You Know?

NDN does not fundamentally ask "Where is the server?"

It asks "Where can I obtain this named data?"

This means the same content could potentially be served by the original producer, a nearby cache, or another authorized source.



---

Quick Recap (Mnemonic)

Name → Request → Retrieve → Cache

Data → Interest → Source → Store




---

THANK YOU!

~ V1NNN22