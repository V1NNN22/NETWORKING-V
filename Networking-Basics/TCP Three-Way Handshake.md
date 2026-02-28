# TCP Three-Way Handshake  
~
## Written By: VINOD N. RATHOD.  
~

## What is the TCP Three-Way Handshake?  
- **Definition:** A connection establishment process used by TCP to create a reliable communication session between client and server.  
- **Purpose:** Ensures both devices are synchronized and ready before actual data transmission begins → prevents data loss and confusion.  
- **Analogy:** Like two people agreeing to talk on a phone call before starting the conversation.  

---

## The 3 Steps of TCP Handshake  

### 1. SYN (Step 1)  
- **Function:** Client sends a synchronization packet to server.  
- **Role:** Requests connection and shares initial sequence number.  
- **Examples:** Client → Server: SYN = 1.  

---

### 2. SYN-ACK (Step 2)  
- **Function:** Server acknowledges request and sends its own SYN.  
- **Role:** Confirms readiness and synchronization.  
- **Examples:** Server → Client: SYN = 1, ACK = 1.  

---

### 3. ACK (Step 3)  
- **Function:** Client sends acknowledgment back to server.  
- **Role:** Finalizes connection establishment.  
- **Examples:** Client → Server: ACK = 1.  

---

## Why It Matters  
- **Reliability:** Ensures both sides agree on sequence numbers.  
- **Error Prevention:** Avoids half-open or ghost connections.  
- **Security Insight:** Helps detect SYN flood attacks.  

---

## Quick Recap (Mnemonic)  
- **Synchronize → Synchronize-Acknowledge → Acknowledge**  
  - **SYN → SYN-ACK → ACK**    

---

# THANK YOU!  
# ~ **V1NNN22**