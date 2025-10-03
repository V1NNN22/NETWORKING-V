# 🚚 OSI Model – Layer 4 (Transport Layer)

Written By: Vinod N. Rathod  

---

## 📌 What is the Transport Layer?  
- **Definition:** The Transport Layer is the fourth layer of the OSI model.  
  It is responsible for providing **end-to-end communication, reliability, and error recovery** between applications running on different devices.  

- **Purpose:**  
  Ensures that data is delivered **completely, correctly, and in the right order** from the sender’s application to the receiver’s application.  

---

## 🔑 Key Functions of the Transport Layer  

### 1️⃣ Segmentation & Reassembly  
- Breaks large data into **smaller segments** for transmission.  
- Reassembles them correctly at the destination.  

### 2️⃣ Error Detection & Recovery  
- Ensures data arrives **without errors**.  
- Retransmits lost or corrupted data if needed.  

### 3️⃣ Flow Control  
- Prevents the sender from overwhelming the receiver with too much data.  
- Uses techniques like **windowing**.  

### 4️⃣ Connection Establishment & Termination  
- Creates reliable communication sessions between devices.  
- Uses the **3-way handshake** in TCP.  

### 5️⃣ Multiplexing  
- Allows **multiple applications** to use the network simultaneously.  
- Achieved through **port numbers** (e.g., port 80 = HTTP, port 25 = SMTP).  

---

## 🖥️ Devices Operating at the Transport Layer  
- **Gateways**  
*(Mostly handled by software in end systems rather than physical devices.)*  

---

## 📡 Examples of Transport Layer Protocols  
- **TCP (Transmission Control Protocol):** Reliable, connection-oriented.  
- **UDP (User Datagram Protocol):** Fast, connectionless, but unreliable.  
- **SCTP (Stream Control Transmission Protocol):** Combines features of TCP & UDP.  

---

## ⚡ Quick Recap (Transport Layer in OSI)  

| **Aspect**   | **Role / Example** |
|--------------|---------------------|
| Data Unit    | Segments |
| Addressing   | Port numbers (application-level addressing) |
| Functions    | Segmentation, error recovery, flow control |
| Reliability  | TCP (reliable), UDP (unreliable) |
| Protocols    | TCP, UDP, SCTP |

---

### 💡 Key Insight  
⚡ The Transport Layer = **“The layer of reliability & ports”** – It ensures **complete, correct, and orderly delivery** of data between applications.  

---