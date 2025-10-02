# 🌐 OSI Model – Layer 3 (Network Layer)

Written By: Vinod N. Rathod  

---

## 📌 What is the Network Layer?
- **Definition:** The Network Layer is the third layer of the OSI model.  
  It is responsible for **logical addressing, routing, and forwarding** of packets across different networks.  

- **Purpose:**  
  Ensures that data is delivered from the **source device** to the **destination device**, even if they are on **different networks**.  

---

## 🔑 Key Functions of the Network Layer  

### 1️⃣ Logical Addressing  
- Assigns unique **logical addresses (IP addresses)** to devices.  
- Differentiates between **source** and **destination** devices.  

### 2️⃣ Routing  
- Determines the **best path** for data to travel across multiple networks.  
- Uses **routing algorithms and protocols** to make decisions.  

### 3️⃣ Packet Forwarding  
- Moves **packets** from one network to another towards the destination.  

### 4️⃣ Fragmentation & Reassembly  
- Splits large packets into **smaller ones** to fit the transmission medium.  
- Reassembles them at the destination.  

### 5️⃣ Error Handling & Diagnostics  
- Detects **unreachable destinations** and provides error messages.  
- **Tools/Protocols:** ICMP (ping, traceroute).  

---

## 🖥️ Devices Operating at the Network Layer  
- Routers  
- Layer 3 Switches  
- Firewalls *(partially, for packet inspection)*  

---

## 📡 Examples of Network Layer Protocols  
- **IP (Internet Protocol)** – IPv4 / IPv6  
- **ICMP (Internet Control Message Protocol)**  
- **ARP (Address Resolution Protocol)**  
- **OSPF (Open Shortest Path First)**  
- **BGP (Border Gateway Protocol)**  
- **RIP (Routing Information Protocol)**  

---

## ⚡ Quick Recap (Network Layer in OSI)

| **Aspect**   | **Role / Example** |
|--------------|---------------------|
| Data Unit    | Packets |
| Addressing   | Logical (IP addresses) |
| Functions    | Routing, forwarding, fragmentation |
| Devices      | Routers, Layer 3 switches |
| Protocols    | IP, ICMP, OSPF, BGP, RIP |

---

### 💡 Key Insight  
⚡ The Network Layer = **“The layer of IP addresses & routing”** – It decides **where the data should go** and **how it will get there**.  

---