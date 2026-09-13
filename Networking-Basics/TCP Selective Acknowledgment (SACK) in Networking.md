---

# TCP Selective Acknowledgment (SACK) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is TCP Selective Acknowledgment (SACK)?  
- **Definition:** TCP Selective Acknowledgment (SACK) is a TCP feature that allows the receiver to inform the sender about exactly which data segments have arrived successfully.
- **Purpose:** It helps TCP retransmit only the missing segments instead of retransmitting the entire data window.
- **Analogy:** If several pages of a document are delivered but pages 4 and 7 are missing, SACK tells the sender to resend only those missing pages.

---  

## The 4 Core Steps of TCP SACK Operation  

### 1. TCP Connection Negotiation  
- **Function:** SACK capability is negotiated during the TCP three-way handshake.
- **Role:** Both endpoints confirm whether they support selective acknowledgment.
- **Examples:** The SACK Permitted option is exchanged in SYN and SYN-ACK packets.

---  

### 2. Out-of-Order Segment Reception  
- **Function:** The receiver accepts segments that arrive out of order.
- **Role:** It stores received segments temporarily instead of discarding them.
- **Examples:** Segments 1, 2, 4, and 5 arrive while segment 3 is missing.

---  

### 3. SACK Information Transmission  
- **Function:** The receiver sends acknowledgment information describing the successfully received data blocks.
- **Role:** It identifies which byte ranges are already available at the receiver.
- **Examples:** The acknowledgment may indicate that segments 4 and 5 arrived even though segment 3 is missing.

---  

### 4. Selective Retransmission  
- **Function:** The sender retransmits only the missing data segments.
- **Role:** It reduces unnecessary traffic and improves recovery from packet loss.
- **Examples:** Only segment 3 is retransmitted instead of sending segments 3, 4, and 5 again.

---  

## Key Features  
- **Efficient Recovery:** Retransmits only missing segments.
- **Reduced Bandwidth Usage:** Avoids duplicate retransmissions.
- **Improved Performance:** Works especially well on high-latency networks.
- **Out-of-Order Handling:** Allows receivers to track successfully received data blocks.

---  

## Why It Matters  
- **High-Speed Networks:** Improves TCP performance over fast connections.
- **Packet Loss Recovery:** Minimizes the impact of multiple lost segments.
- **Long-Distance Communication:** Useful where retransmission delays are significant.
- **Network Efficiency:** Prevents unnecessary duplicate data transmission.

---  

## Quick Recap (Mnemonic)  
- **N → R → S → T**  
  - **Negotiate → Receive Out-of-Order → Send SACK → Retransmit Missing Data**  

---  


# THANK YOU!  
# ~ **V1NNN22**