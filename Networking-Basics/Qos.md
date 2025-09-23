# QoS (Quality of Service)  
~
## Written By: VINOD N. RATHOD.  
~

---

## 📌 What is QoS?  
- **Definition:** QoS is a **network feature** that manages and prioritizes network traffic to ensure the performance of critical applications and maintain acceptable levels of **latency, jitter, and packet loss**.  
- **Purpose:**  
  - Guarantees **bandwidth** for high-priority applications (e.g., VoIP, video conferencing).  
  - Reduces **latency** and **jitter** for sensitive traffic.  
  - Ensures **reliable network performance** for critical services.  
- **Layer:** Operates mainly at the **Network Layer (Layer 3)**, but also involves **Data Link Layer (Layer 2)** mechanisms.  

---

## ⚙️ Key QoS Parameters  
1. **Bandwidth** – Maximum rate of data transfer on a network path.  
2. **Latency** – Time it takes for a packet to travel from source to destination.  
3. **Jitter** – Variability in packet delay over time.  
4. **Packet Loss** – Percentage of packets lost during transmission.  

---

## 🛠️ QoS Techniques  
1. **Traffic Classification** – Identifies and labels traffic based on type or priority.  
2. **Traffic Shaping** – Delays lower-priority traffic to smooth bursts.  
3. **Traffic Policing** – Drops or marks packets that exceed set limits.  
4. **Prioritization / Queuing** – High-priority traffic gets faster forwarding (e.g., VoIP over web browsing).  
5. **Resource Reservation (RSVP)** – Reserves bandwidth for specific flows in the network.  

---

## 📡 QoS Models  
1. **Integrated Services (IntServ)** – Reserves resources per flow; suitable for real-time applications.  
2. **Differentiated Services (DiffServ)** – Marks packets into classes; routers prioritize based on class.  
3. **Best Effort** – No QoS guarantees; traffic treated equally.  

---

## ⚡ Quick Recap (QoS)  

| Concept       | Meaning |
|---------------|---------|
| **QoS**       | Manages network traffic to prioritize critical applications |
| **Bandwidth** | Max data rate available |
| **Latency**   | Time taken for packet delivery |
| **Jitter**    | Variation in packet delay |
| **Packet Loss** | Percentage of lost packets |
| **Techniques** | Classification, Shaping, Policing, Prioritization |
| **Models**    | IntServ, DiffServ, Best Effort |

---

![Diagram](Assets/qos.png)  

---

# THANK YOU!  
# ~ **V1NNN22**