# Bridges and Gateways  
~
## Written By: VINOD N. RATHOD.  
~

---

## 🌉 What is a Bridge?  
- **Definition:** A bridge is a networking device that connects and filters traffic between two or more **LAN segments**.  
- **Purpose:** Reduces network collisions and divides large networks into smaller, more efficient segments.  
- **Layer:** Operates at the **Data Link Layer (Layer 2)** of the OSI model.  

### 🔑 Functions  
- Learns and forwards based on **MAC addresses**.  
- Improves performance by **isolating traffic**.  
- Can connect different physical mediums (e.g., **wired ↔ wireless**).  

---

### 🏗️ Types of Bridges  

#### 1. Transparent Bridge  
- Common in **Ethernet networks**.  
- Forwards frames after learning **MAC addresses** automatically.  

#### 2. Translational Bridge  
- Connects networks using different technologies (e.g., **Ethernet ↔ Token Ring**).  

#### 3. Source-Route Bridge  
- Used in **Token Ring networks**.  
- The **sending device specifies the route** for the frame.  

---

## 🌐 What is a Gateway?  
- **Definition:** A gateway is a network device that connects **two different networks** that use different protocols.  
- **Purpose:** Acts as a **translator** between networks so they can communicate.  
- **Layer:** Can operate at **any layer** of the OSI model, often at the **Application Layer**.  

### 🔑 Functions  
- **Protocol conversion** (e.g., IPv4 ↔ IPv6, Email ↔ SMS).  
- Connects **dissimilar systems** (LAN ↔ mainframe, LAN ↔ cloud).  
- Often implemented in **routers, firewalls, or dedicated appliances**.  

---

### ⚙️ Examples of Gateways  

1. **Default Gateway**  
   - The **router IP address** that connects a local network to the Internet.  

2. **VoIP Gateway**  
   - Converts voice signals between **traditional phone lines ↔ IP networks**.  

3. **Email Gateway**  
   - Filters and transfers **emails** between different mail systems.  

4. **Cloud Gateway**  
   - Connects **on-premise networks ↔ cloud services**.  

---

## ⚡ Quick Recap (Bridge vs Gateway)  

| Feature     | Bridge | Gateway |
|-------------|--------|---------|
| **OSI Layer** | Layer 2 (Data Link) | Any layer (often Application Layer) |
| **Purpose**   | Connects & filters LAN segments | Connects different networks/protocols |
| **Works On**  | MAC addresses | Protocol conversion / translation |
| **Example**   | Ethernet bridge, Wireless bridge | Default gateway, VoIP gateway, Email GW |

---

![Diagram](Assets/bridge-gateway.png)  

---

# THANK YOU!  
# ~ **V1NNN22**