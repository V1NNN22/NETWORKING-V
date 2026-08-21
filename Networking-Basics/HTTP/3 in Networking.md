# HTTP/3 in Networking
~
## Written By: VINOD N. RATHOD.
~

## What is HTTP/3?
- **Definition:** HTTP/3 is the third major version of HTTP that uses QUIC over UDP instead of TCP as its transport protocol.
- **Purpose:** Improves web performance by combining HTTP with QUIC's encrypted transport, stream multiplexing, and faster connection establishment.
- **Analogy:** Traditional HTTP/2 is like several delivery trucks sharing one highway where one major accident can block everyone. HTTP/3 gives each stream a more independent lane so a problem with one stream does not necessarily stop the others.

---

## The 4 Core Steps of HTTP/3 Operation

### 1. QUIC Connection Establishment (Step 1)
- **Function:** The client establishes a QUIC connection with the HTTP/3 server.
- **Role:** Provides encrypted transport using TLS 1.3.
- **Examples:** A browser connects to a website using QUIC over UDP port 443.

---

### 2. HTTP Request Transmission (Step 2)
- **Function:** HTTP requests are carried through QUIC streams.
- **Role:** Allows application data to be exchanged without relying on TCP.
- **Examples:** A browser requests an HTML page, stylesheet, or API resource.

---

### 3. Stream Multiplexing (Step 3)
- **Function:** Multiple HTTP requests and responses can use independent QUIC streams within the same connection.
- **Role:** Prevents packet loss affecting one stream from blocking unrelated streams at the transport level.
- **Examples:** An image download can experience packet loss without necessarily blocking a JavaScript stream.

---

### 4. Reliable Data Delivery (Step 4)
- **Function:** QUIC provides reliable delivery, congestion control, and retransmission for each stream.
- **Role:** Ensures HTTP data arrives correctly while maintaining efficient network performance.
- **Examples:** Lost packets are recovered without requiring the entire connection to stop.

---

## Key Features
- **QUIC-Based:** Uses QUIC instead of TCP.
- **TLS 1.3 Security:** Encryption is integrated into the transport.
- **Stream Multiplexing:** Supports multiple independent streams.
- **Reduced Head-of-Line Blocking:** Packet loss on one stream does not block unrelated streams at the QUIC transport level.
- **Connection Migration:** Connections can survive changes such as switching from Wi-Fi to mobile data.
- **Fast Connection Setup:** Reduces connection establishment overhead.

---

## Why It Matters
- **Faster Web Applications:** Reduces latency for modern web traffic.
- **Better Mobile Performance:** Handles changing network paths more gracefully.
- **Improved Multiplexing:** Reduces the impact of packet loss on unrelated streams.
- **Modern Transport:** Combines HTTP semantics with QUIC's modern transport features.
- **Internet Evolution:** Moves web transport beyond the traditional TCP-based architecture.

---

## Quick Recap (Mnemonic)
- **Connect → Request → Multiplex → Deliver**
  - **QUIC → HTTP → Streams → Data**

---


# THANK YOU!
# ~ **V1NNN22**