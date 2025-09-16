# Network Address Translation (NAT)  
~
## Written By: VINOD N. RATHOD.  
~

---

## 🌍 What is NAT?  
- **Definition:** NAT is a method used by **routers/firewalls** to translate **private IP addresses** within a LAN into a **public IP address** (and vice versa) for communication over the Internet.  
- **Purpose:** Allows multiple devices in a private network to **share a single public IP address**.  
- **Layer:** Operates at the **Network Layer (Layer 3)** of the OSI model.  

---

## ❓ Why NAT is Needed?  
- IPv4 addresses are **limited (~4.3 billion total)**.  
- NAT helps **conserve public IP addresses**.  
- Provides a layer of **security** (hides internal IPs from the outside world).  

---

## 🛠️ Types of NAT  

### 1. Static NAT (SNAT)  
- One **private IP ↔ one public IP** (one-to-one mapping).  
- Used when a device inside the LAN needs to be **accessible from outside** (e.g., web server).  

---

### 2. Dynamic NAT (DNAT)  
- Private IPs are mapped to available **public IPs from a pool**.  
- Mapping changes **dynamically** depending on availability.  

---

### 3. PAT (Port Address Translation) / NAT Overload  
- Many private IPs share **one public IP**, differentiated by **port numbers**.  
- Most common form of NAT (**used in home routers**).  
- **Example:** Multiple devices browsing the Internet through one ISP-provided IP.  

---

## ✅ Advantages of NAT  
- Conserves **public IP addresses**.  
- Adds **privacy/security** (internal IPs hidden).  
- Flexible — supports both **static and dynamic mappings**.  

---

## ⚠️ Disadvantages of NAT  
- Can cause **delays** due to translation overhead.  
- Some applications (**VoIP, peer-to-peer**) may face issues.  
- Breaks **true end-to-end connectivity**.  

---

## ⚡ Quick Recap (Types of NAT)  

| Type         | Mapping                  | Use Case |
|--------------|--------------------------|----------------------------------|
| **Static NAT**   | One private ↔ One public   | Hosting servers inside LAN |
| **Dynamic NAT**  | Private ↔ Public pool      | Enterprises with multiple available IPs |
| **PAT / Overload** | Many private ↔ One public | Home/office Internet sharing |

---

![Diagram](Assets/nat.png)  

---

# THANK YOU!  
# ~ **V1NNN22**