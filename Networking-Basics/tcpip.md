
# TCP/IP Model (4 Layers)  
~
## Written By: VINOD N. RATHOD.  
~

## What is the TCP/IP Model?  
- **Definition:** A practical communication model developed by the U.S. Department of Defense (DoD) to standardize network communication.  
- **Purpose:** Basis of the modern internet; simpler and more implementation-oriented compared to the OSI model.  
- **Structure:** Has 4 layers instead of 7.  

---

## The 4 Layers of TCP/IP Model  

### 1. Network Access Layer (Link Layer)  
- **Function:** Handles physical transmission of data over the network.  
- **Includes:** Hardware addressing, MAC, and protocols like Ethernet/Wi-Fi.  
- **Similar to:** OSI Physical + Data Link layers.  

---

### 2. Internet Layer  
- **Function:** Responsible for logical addressing, routing, and delivering packets across networks.  
- **Protocols:** IP (IPv4/IPv6), ICMP, ARP.  
- **Similar to:** OSI Network layer.  

---

### 3. Transport Layer  
- **Function:** Ensures reliable communication between applications.  
- **Protocols:**  
  - **TCP** → Reliable, connection-oriented.  
  - **UDP** → Fast, connectionless.  
- **Similar to:** OSI Transport layer.  

---

### 4. Application Layer  
- **Function:** Provides services directly to users and applications.  
- **Protocols:** HTTP, FTP, SMTP, DNS, Telnet, etc.  
- **Covers:** OSI Session + Presentation + Application layers.  

---

## TCP/IP vs OSI Model (Comparison Table)  

| Aspect       | OSI Model (7 layers) | TCP/IP Model (4 layers) |
|--------------|-----------------------|--------------------------|
| **Layers**   | Physical, Data Link, Network, Transport, Session, Presentation, Application | Network Access, Internet, Transport, Application |
| **Development** | Conceptual / Theoretical model (ISO standard) | Practical / Implemented model (DoD, Internet) |
| **Approach** | Layered, detailed roles | Simplified, real-world implementation |
| **Transport** | Provides connection-oriented & connectionless | Uses TCP (reliable) & UDP (fast) |
| **Application** | Split into 3 layers | Merged into one layer |
| **Use** | Reference, teaching, design | Used in real-world networking & internet |

---

## Quick Recap  
- **OSI → 7 layers** (theoretical, detailed).  
- **TCP/IP → 4 layers** (practical, real-world).  
- **TCP/IP model is the foundation of the internet.**  

---

![Diagram](Assets/tcpip-model.png)  

---

# THANK YOU!  
# ~ **V1NNN22**  
```

