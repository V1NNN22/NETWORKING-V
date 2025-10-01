

# 🌐 OSI Model – Layer 2 (Data Link Layer)

Written By: Vinod N. Rathod  

---

## 📌 What is the Data Link Layer?
- **Definition:** The Data Link Layer is the second layer of the OSI (Open Systems Interconnection) model.  
  It is responsible for **node-to-node data transfer** and **error detection/correction** across the physical link.  

- **Purpose:**  
  Ensures that data is transferred **reliably and correctly** between two directly connected devices on the same network.  

---

## 🔑 Key Functions of the Data Link Layer  

### 1️⃣ Framing
- Converts raw bits from the Physical Layer into **frames** (structured data units).  
- Adds **headers and trailers** for proper delivery.  

### 2️⃣ Error Detection & Correction
- Detects errors during transmission.  
- **Techniques:** CRC (Cyclic Redundancy Check), checksums.  

### 3️⃣ Flow Control
- Prevents a **fast sender** from overwhelming a **slow receiver**.  

### 4️⃣ MAC (Media Access Control)
- Determines how devices access the **physical medium**.  
- Ensures only one device transmits at a time (**collision avoidance**).  

### 5️⃣ Addressing
- Uses **MAC addresses** (48-bit unique identifiers) to identify devices.  
- Ensures correct **destination delivery** within the same network.  

---

## 🧩 Sublayers of the Data Link Layer  

### 🔹 LLC (Logical Link Control)  
- Manages **flow control** and **error checking**.  
- Provides the interface between the **Network Layer** and **MAC sublayer**.  

### 🔹 MAC (Media Access Control)  
- Controls access to the **physical medium**.  
- Handles **hardware addressing (MAC addresses)**.  

---

## 🖥️ Devices Operating at the Data Link Layer
- Switches  
- Bridges  
- Network Interface Cards (NICs) *(partially operate here too)*  

---

## 📡 Examples of Data Link Layer Protocols
- **Ethernet (IEEE 802.3)**  
- **Wi-Fi (IEEE 802.11)**  
- **PPP (Point-to-Point Protocol)**  
- **HDLC (High-Level Data Link Control)**  
- **Frame Relay**  

---

## ⚡ Quick Recap (Data Link Layer in OSI)

| **Aspect**    | **Role / Example** |
|---------------|---------------------|
| Data Unit     | Frames |
| Addressing    | MAC addresses (Layer 2 addressing) |
| Functions     | Framing, error detection, flow control |
| Devices       | Switches, bridges, NICs |
| Protocols     | Ethernet, Wi-Fi, PPP, HDLC |

---

### 💡 Key Insight  
⚡ The Data Link Layer = **“The layer of frames & MAC addresses”** – It makes raw transmission **reliable and organized**.  

---

