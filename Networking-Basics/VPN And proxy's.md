# VPN and Proxies  
~
## Written By: VINOD N. RATHOD.  
~

---

## 🔒 What is a VPN (Virtual Private Network)?  
- **Definition:** A VPN is a secure connection that creates an **encrypted tunnel** between a user’s device and a remote server/network.  
- **Purpose:** Protects **data privacy**, hides **IP addresses**, and allows **secure remote access**.  
- **Layer:** Works at the **Network Layer (Layer 3)** using **tunneling protocols**.  

---

## 🌐 Types of VPN  

### 1. Remote Access VPN  
- Allows **individual users** to connect securely to a remote network.  
- Example: Employees working from home.  

### 2. Site-to-Site VPN  
- Connects **entire networks** at different locations over the Internet.  
- Commonly used between **branch offices** and **headquarters**.  

### 3. Client-to-Site VPN  
- A specific **device (client)** securely connects to a **company network**.  

---

## 📡 Common VPN Protocols  
- **PPTP (Point-to-Point Tunneling Protocol)**  
- **L2TP/IPsec (Layer 2 Tunneling Protocol with IPsec)**  
- **OpenVPN (SSL/TLS based, widely used)**  
- **IKEv2/IPsec**  
- **WireGuard (modern, fast, secure)**  

---

## 🖥️ What is a Proxy Server?  
- **Definition:** A proxy acts as an **intermediary** between a client and the Internet.  
- **Purpose:** Hides client’s **IP address**, filters requests, caches content, and can **bypass restrictions**.  
- **Layer:** Works at the **Application Layer (Layer 7)**.  

---

## 🛠️ Types of Proxies  

### 1. Forward Proxy  
- Used by **clients** to access the Internet indirectly.  
- Can restrict/block content and **log traffic**.  

### 2. Reverse Proxy  
- Sits **in front of servers** to handle requests on their behalf.  
- Provides **load balancing**, **caching**, and **security**.  

### 3. Transparent Proxy  
- Clients are **unaware** of proxy use.  
- Common in **ISP-level content filtering**.  

### 4. Anonymous & High-Anonymity Proxies  
- **Anonymous:** Hides client identity.  
- **High-Anonymity:** Completely masks client’s identity from target servers.  

---

## ⚡ VPN vs Proxy (Quick Comparison)  

| Feature  | VPN | Proxy |
|----------|-----|-------|
| **Security** | Encrypts all traffic (end-to-end) | Usually no encryption (just hides IP) |
| **Scope** | Whole device (system-wide) | Application-specific (browser, app) |
| **OSI Layer** | Network Layer (L3) | Application Layer (L7) |
| **Speed** | Slightly slower (encryption overhead) | Faster, but less secure |
| **Use Case** | Secure remote access, privacy, bypass | Bypass restrictions, content filtering |

---

![Diagram](Assets/vpn_proxy.png)  

---

# THANK YOU!  
# ~ **V1NNN22**