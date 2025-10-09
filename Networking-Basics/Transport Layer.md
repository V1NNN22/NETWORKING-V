

## 🚀 TCP/IP Model – Layer 3 (Transport Layer)

##**Written By:** Vinod N. Rathod  



## 📘 What is the Transport Layer?

**Definition:**  
The **Transport Layer** is the **third layer** of the TCP/IP model.  
It is responsible for providing **end-to-end communication**, **reliability**, and **flow control** between applications running on different devices.

**Purpose:**  
Ensures that data is delivered **accurately**, **completely**, and **in the correct order** between the source and destination applications.

---

## ⚙️ Key Functions of the Transport Layer

### 1️⃣ Segmentation & Reassembly
- Breaks large data from applications into smaller **segments** for transmission.  
- **Reassembles** these segments in the correct order at the destination.

---

### 2️⃣ Error Detection & Recovery
- Detects **lost or corrupted** data during transmission.  
- Performs **retransmission** of data if errors occur (in TCP).

---

### 3️⃣ Flow Control
- Manages data flow between sender and receiver to **prevent overload**.  
- Uses techniques such as **windowing** to regulate data rate.

---

### 4️⃣ Connection Management
- Establishes, maintains, and terminates **reliable communication sessions**.  
- Uses the **three-way handshake** mechanism in TCP.

---

### 5️⃣ Multiplexing
- Enables multiple applications to share the same network connection.  
- Uses **port numbers** to identify specific application processes (e.g., 80 = HTTP, 443 = HTTPS).

---

## 🖥️ Devices Operating at the Transport Layer
- **Gateways**  
- **Firewalls** (for port-based filtering)  
- Mostly handled by **software at the OS or application level**

---

## 🌐 Examples of Transport Layer Protocols

| **Protocol** | **Description** |
|---------------|------------------|
| **TCP (Transmission Control Protocol)** | Reliable, connection-oriented communication |
| **UDP (User Datagram Protocol)** | Fast, connectionless, and lightweight communication |
| **SCTP (Stream Control Transmission Protocol)** | Combines reliability of TCP with features of UDP |

---

## ⚡ Quick Recap (Transport Layer in TCP/IP)

| **Aspect** | **Role / Example** |
|-------------|--------------------|
| **Data Unit** | Segments |
| **Addressing** | Port Numbers |
| **Functions** | Segmentation, reliability, flow control |
| **Protocols** | TCP, UDP, SCTP |
| **Reliability Type** | TCP = Reliable, UDP = Unreliable |

---

### 💡 The Transport Layer = “The Layer of Reliability & Ports”  
⚡ It ensures **end-to-end communication** between applications and manages the **quality of data delivery**.

---
# ~ V1NNN22 ~
# THANKYOU! 