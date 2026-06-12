# TCP SYN Cookies in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What are TCP SYN Cookies?  
- **Definition:** SYN Cookies are a defense mechanism used to protect servers from TCP SYN Flood attacks.
- **Purpose:** Allows a server to handle connection requests without storing state information immediately.
- **Simple Meaning:** Verify the client before reserving resources.

---

## The 4 Core Steps of SYN Cookies

### 1. SYN Request Received (Step 1)
- **Function:** Client sends a TCP SYN packet.
- **Role:** Initiates connection.

---

### 2. Cookie Generation (Step 2)
- **Function:** Server generates a special sequence number.
- **Role:** Encodes connection information into the SYN-ACK.

---

### 3. Client Response (Step 3)
- **Function:** Client replies with ACK.
- **Role:** Proves it received the SYN-ACK.

---

### 4. Connection Creation (Step 4)
- **Function:** Server validates the cookie.
- **Result:** Resources allocated only for legitimate clients.

---

## Why SYN Cookies Exist
- **Prevent SYN Flood attacks**
- **Reduce memory exhaustion**
- **Protect TCP services**
- **Maintain availability during attacks**

---

## Real-World Attack Without SYN Cookies

### Attacker Sends
```text
Millions of SYN packets
```

### Server Action
```text
Allocates memory for each request
```

### Result
```text
Connection table fills up
```

### Impact
```text
Legitimate users denied access
```

---

## TCP Handshake

### Normal Process
```text
SYN
SYN-ACK
ACK
```

### With SYN Cookies
```text
SYN
SYN-ACK (Cookie)
ACK (Validation)
```

---

## Detection

### Check SYN Cookie Status (Linux)
```bash
sysctl net.ipv4.tcp_syncookies
```

---

### View Connection States
```bash
netstat -ant
```

---

### Monitor SYN Queue
```bash
ss -s
```

---

## Configuration

### Enable SYN Cookies
```bash
sysctl -w net.ipv4.tcp_syncookies=1
```

---

### Permanent Configuration
```bash
net.ipv4.tcp_syncookies = 1
```

---

## Advantages

### Security
```text
Mitigates SYN floods
```

### Efficiency
```text
No early resource allocation
```

### Availability
```text
Keeps services online
```

---

## Key Features
- TCP protection mechanism
- Stateless validation
- Defends against SYN floods
- Lightweight implementation

---

## Why It Matters
- **Protects public-facing servers**
- **Improves service availability**
- **Reduces DoS impact**
- **Fundamental TCP defense**

---

## Quick Recap
**SYN → Cookie → ACK → Connect**
**Request → Verify → Validate → Allocate**

---

# THANK YOU!
# ~ **V1NNN22**