# TCP Selective Acknowledgment (SACK) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is TCP SACK?  
- **Definition:** TCP Selective Acknowledgment (SACK) allows a receiver to inform the sender exactly which packets were received successfully.
- **Purpose:** Improves recovery from packet loss.
- **Simple Meaning:** Instead of saying "I missed something," TCP says "I missed packet #5, but I got #6, #7, and #8."

---

## The 4 Core Steps of TCP SACK

### 1. Data Transmission (Step 1)
- **Function:** Sender transmits multiple TCP segments.
- **Role:** Deliver application data.

---

### 2. Packet Loss Occurs (Step 2)
- **Function:** One or more packets are lost in transit.
- **Role:** Creates a gap in received data.

---

### 3. SACK Information Sent (Step 3)
- **Function:** Receiver informs sender which blocks arrived successfully.
- **Role:** Pinpoints missing packets.

---

### 4. Selective Retransmission (Step 4)
- **Function:** Sender retransmits only missing packets.
- **Result:** Faster recovery and better efficiency.

---

## Why TCP SACK Exists
- **Reduces unnecessary retransmissions**
- **Improves WAN performance**
- **Handles packet loss efficiently**
- **Increases throughput**

---

## Real-World Example

### Packets Sent
```text
1 2 3 4 5 6 7 8
```

### Packet Lost
```text
5
```

### Receiver Gets
```text
1 2 3 4 6 7 8
```

### SACK Reply
```text
Missing Packet 5
```

### Result
```text
Only Packet 5 retransmitted
```

---

## Without SACK

### Packet Lost
```text
5
```

### Sender Action
```text
Retransmit 5 6 7 8
```

### Result
```text
Bandwidth wasted
```

---

## With SACK

### Packet Lost
```text
5
```

### Sender Action
```text
Retransmit 5
```

### Result
```text
Efficient recovery
```

---

## Detection

### Linux
```bash
sysctl net.ipv4.tcp_sack
```

---

### Packet Capture
```bash
tcpdump -i eth0
```

Look for:
```text
SACK Permitted
```

---

## Configuration

### Enable SACK
```bash
sysctl -w net.ipv4.tcp_sack=1
```

---

### Permanent Configuration
```bash
net.ipv4.tcp_sack = 1
```

---

## SACK vs Traditional TCP

### Traditional TCP
```text
Retransmit many packets
```

### TCP SACK
```text
Retransmit only missing packets
```

---

## Key Features
- Efficient packet recovery
- Better WAN performance
- Reduced retransmissions
- Higher throughput

---

## Why It Matters
- **Improves TCP efficiency**
- **Reduces bandwidth waste**
- **Speeds recovery from packet loss**
- **Critical for modern Internet traffic**

---

## Quick Recap
**Send → Lose → Report → Retransmit**
**Packet Loss → SACK → Missing Packet → Recovery**

---

# THANK YOU!
# ~ **V1NNN22**