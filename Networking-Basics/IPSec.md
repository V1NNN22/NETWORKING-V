# 🔐 IPSec (Internet Protocol Security)  
~
## Written By: VINOD N. RATHOD  
~

---

## 📌 What is IPSec?  
- **Definition:** IPSec is a suite of protocols used to **secure IP communications** by authenticating and encrypting each IP packet in a data stream.  
- **Purpose:**  
  - Provides **confidentiality, integrity, and authentication** of data.  
  - Protects information traveling across **untrusted networks** (e.g., the Internet).  
  - Commonly used in **VPNs (Virtual Private Networks)**.  
- **Layer:** Works at the **Network Layer (Layer 3)** of the OSI model.  

---

## 🛡️ Key Features of IPSec  
1. **Confidentiality** – Encrypts data to prevent eavesdropping.  
2. **Integrity** – Ensures data is not altered in transit.  
3. **Authentication** – Verifies identities of sender & receiver.  
4. **Anti-Replay Protection** – Blocks attackers from reusing captured packets.  

---

## ⚙️ IPSec Protocols  
- **AH (Authentication Header):**  
  - Provides **authentication & integrity**.  
  - ❌ Does not provide encryption.  

- **ESP (Encapsulating Security Payload):**  
  - Provides **authentication, integrity, AND encryption**.  
  - ✅ Most widely used in VPNs.  

---

## 🔀 IPSec Modes  

| **Mode**          | **What it Encrypts**       | **Use Case**              |
|-------------------|-----------------------------|---------------------------|
| **Transport Mode**| Only the **payload** (data) | End-to-end (Host ↔ Host) |
| **Tunnel Mode**   | Entire IP packet (Header + Payload) | Site-to-Site VPNs (Routers/Firewalls) |

---

## 🔑 IPSec Key Management  
- Uses **IKE (Internet Key Exchange)** protocol.  
- Automates **key exchange** and negotiates **Security Associations (SAs)**.  

---

## ✅ Advantages of IPSec  
- Provides **strong network-layer security**.  
- Works transparently with applications.  
- Standard choice for **secure VPN tunnels**.  

---

## ⚠️ Disadvantages of IPSec  
- Higher **CPU usage** due to encryption/decryption.  
- May cause **performance overhead**.  
- Configuration can be **complex** compared to other security solutions.  

---

## ⚡ Quick Recap (IPSec)  

| **Concept**       | **Meaning** |
|-------------------|-------------|
| **IPSec**         | Suite of protocols for secure IP communication |
| **AH**            | Authentication & integrity only |
| **ESP**           | Encryption + authentication + integrity |
| **Transport Mode**| Encrypts only payload (end-to-end) |
| **Tunnel Mode**   | Encrypts entire packet (site-to-site VPNs) |
| **IKE**           | Handles key exchange & SAs |

---

![IPSec Diagram](Assets/ipsec-diagram.png)  

---

# THANK YOU!  
# ~ **V1NNN22**