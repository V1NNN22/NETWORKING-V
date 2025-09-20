# Types of Firewalls  
~
## Written By: VINOD N. RATHOD.  
~

---

## 🔒 What is a Firewall?  
- **Definition:** A firewall is a **network security device or software** that monitors and controls **incoming and outgoing network traffic** based on predefined security rules.  
- **Purpose:**  
  - Protects networks from **unauthorized access**.  
  - Blocks **malicious traffic and attacks**.  
  - Enforces **security policies**.  
- **Layer:** Works at **multiple OSI layers** depending on type (Network, Transport, Application).  

---

## 🛠️ Types of Firewalls  

### 1. Packet-Filtering Firewall  
- Examines **packets individually**.  
- Allows or blocks based on **source/destination IP, port, or protocol**.  
- Fast but basic; cannot detect **complex attacks**.  

### 2. Stateful Inspection Firewall  
- Tracks the **state of active connections**.  
- Makes decisions based on **context** (state of the connection).  
- More secure than packet-filtering firewalls.  

### 3. Proxy Firewall (Application-Level Firewall)  
- Works at the **Application Layer**.  
- Acts as an **intermediary between client and server**.  
- Can inspect **application-specific traffic** (HTTP, FTP, etc.).  

### 4. Next-Generation Firewall (NGFW)  
- Combines traditional firewall with **advanced features**:  
  - Intrusion Prevention System (IPS)  
  - Deep Packet Inspection  
  - Application awareness  
- Provides **stronger protection** for modern threats.  

### 5. Network Address Translation (NAT) Firewall  
- Hides **internal IP addresses** from external networks.  
- Provides **basic security** and **IP conservation**.  

---

## 🖥️ Firewall Deployment Modes  
- **Network-Based Firewall:** Protects the **entire network**.  
- **Host-Based Firewall:** Installed on **individual devices** to protect them.  

---

## ⚡ Quick Recap (Firewalls)  

| Concept                  | Meaning |
|--------------------------|---------|
| **Firewall**             | Device/software protecting network traffic |
| **Packet Filtering**      | Blocks/accepts packets based on rules |
| **Stateful Inspection**   | Tracks connection state for security |
| **Proxy Firewall**        | Acts as intermediary, inspects applications |
| **NGFW**                  | Advanced firewall with integrated security features |
| **NAT Firewall**          | Hides internal IPs, basic security |

---

![Diagram](Assets/firewall_types.png)  

---

# THANK YOU!  
# ~ **V1NNN22**