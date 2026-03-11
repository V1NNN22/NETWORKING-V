# TCP vs UDP (Transport Protocols)  
~
## Written By: VINOD N. RATHOD.  
~

## What are TCP and UDP?  
- **Definition:** Two core transport layer protocols used to transmit data between devices over a network.  
- **Purpose:** Provide different communication styles depending on reliability and speed requirements.  
- **Analogy:** TCP is like a registered courier with confirmation, while UDP is like sending a postcard without tracking.  

---

## The 4 Key Differences Between TCP and UDP  

### 1. Connection Type  
- **TCP Function:** Connection-oriented communication.  
- **Role:** Establishes a session before sending data.  
- **Examples:** Web browsing (HTTP/HTTPS), file transfer.  

- **UDP Function:** Connectionless communication.  
- **Role:** Sends data without establishing a connection.  
- **Examples:** Streaming, gaming, VoIP.  

---

### 2. Reliability  
- **TCP Function:** Ensures reliable delivery.  
- **Role:** Uses acknowledgments, retransmissions, and sequence numbers.  
- **Examples:** Email transmission using SMTP.  

- **UDP Function:** No delivery guarantees.  
- **Role:** Packets may be lost without retransmission.  
- **Examples:** Live video streaming.  

---

### 3. Speed  
- **TCP Function:** Slower due to connection setup and reliability checks.  
- **Role:** Prioritizes accuracy over speed.  

- **UDP Function:** Faster due to minimal overhead.  
- **Role:** Prioritizes speed over reliability.  

---

### 4. Use Cases  
- **TCP Examples:** HTTP, HTTPS, FTP, SSH.  
- **UDP Examples:** DNS queries, online gaming, VoIP calls.  

---

## Key Characteristics  

| Feature | TCP | UDP |
|------|------|------|
| Connection | Connection-oriented | Connectionless |
| Reliability | Reliable | Unreliable |
| Speed | Slower | Faster |
| Packet Order | Guaranteed | Not guaranteed |

---

## Why It Matters  
- **Application Performance:** Different apps require different transport protocols.  
- **Network Efficiency:** UDP reduces overhead for real-time communication.  
- **Reliability Needs:** TCP ensures accurate data delivery.  

---

## Quick Recap (Mnemonic)  
- **Reliable vs Fast**  
  - **TCP → Reliable Communication**  
  - **UDP → Fast Communication**  

---

# THANK YOU!  
# ~ **V1NNN22**