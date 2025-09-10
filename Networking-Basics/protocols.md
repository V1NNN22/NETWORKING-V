# Common Networking Protocols  
~
## Written By: VINOD N. RATHOD.  
~

## What are Protocols?  
- **Definition:** Protocols are standardized rules and conventions that define how data is transmitted and received across networks.  
- **Purpose:** Ensure reliable, secure, and organized communication between devices.  
- **Layer:** Mostly function at the Application Layer (Layer 7 of OSI), though some involve other layers.  

---

## Important Protocols  

### 1. HTTP (HyperText Transfer Protocol)  
- **Layer:** Application  
- **Purpose:** Transfers web pages between client (browser) and server.  
- **Port:** 80  
- **Limitation:** Data sent in plain text (not secure).  

---

### 2. HTTPS (HTTP Secure)  
- **Layer:** Application  
- **Purpose:** Secure version of HTTP, adds encryption (SSL/TLS).  
- **Port:** 443  
- **Use:** Online banking, secure websites, e-commerce.  

---

### 3. FTP (File Transfer Protocol)  
- **Layer:** Application  
- **Purpose:** Transfers files between client and server.  
- **Ports:** 20 (data), 21 (control)  
- **Limitation:** Not secure (can use **SFTP/FTPS** for security).  

---

### 4. SMTP (Simple Mail Transfer Protocol)  
- **Layer:** Application  
- **Purpose:** Sends outgoing emails between mail servers.  
- **Port:** 25 (or 587 with authentication).  

---

### 5. DNS (Domain Name System)  
- **Layer:** Application  
- **Purpose:** Resolves domain names into IP addresses.  
- **Port:** 53  
- **Example:** `www.google.com` → `142.250.190.78`  

---

### 6. DHCP (Dynamic Host Configuration Protocol)  
- **Layer:** Application  
- **Purpose:** Automatically assigns IP addresses, subnet masks, gateways, and DNS info to devices.  
- **Ports:** 67 (server), 68 (client)  

---

### 7. SNMP (Simple Network Management Protocol)  
- **Layer:** Application  
- **Purpose:** Monitors and manages network devices (routers, switches, servers).  
- **Ports:** 161 (queries), 162 (traps)  

---

## Quick Recap (Ports & Uses)  

| Protocol | Port(s)   | Purpose |
|----------|-----------|---------|
| **HTTP** | 80        | Web browsing (insecure) |
| **HTTPS** | 443      | Secure web browsing |
| **FTP**  | 20/21     | File transfer |
| **SMTP** | 25 / 587  | Sending emails |
| **DNS**  | 53        | Domain name → IP resolution |
| **DHCP** | 67 / 68   | Automatic IP address assignment |
| **SNMP** | 161 / 162 | Network device monitoring |

---

![Diagram](Assets/protocols.png)  

---

# THANK YOU!  
# ~ **V1NNN22**  
