# ⚖️ Load Balancer  
~
## Written By: VINOD N. RATHOD  
~

---

## 📌 What is a Load Balancer?  
- **Definition:** A load balancer is a **networking device or software** that distributes incoming traffic across multiple servers.  
- **Purpose:**  
  - Prevents any single server from being overloaded.  
  - Improves **reliability** and **application performance**.  
- **Layer:** Can operate at multiple layers:  
  - **Layer 4 (Transport Layer):** Based on IP address & port.  
  - **Layer 7 (Application Layer):** Based on content (HTTP headers, URLs, cookies, etc.).  

---

## 🛠️ Types of Load Balancers  
1. **Hardware Load Balancer**  
   - Dedicated physical appliances.  
   - High performance, common in large enterprises & data centers.  

2. **Software Load Balancer**  
   - Runs on standard servers (e.g., **HAProxy, Nginx**).  
   - Cost-effective and flexible.  

3. **Cloud Load Balancer**  
   - Provided by cloud providers (**AWS ELB, Azure LB, GCP LB**).  
   - Scalable, pay-as-you-go model.  

---

## 🔀 Load Balancing Algorithms  
- **Round Robin** – Distributes requests one by one in sequence.  
- **Least Connections** – Sends traffic to the server with the fewest active sessions.  
- **IP Hash** – Maps client IP → server (ensures session stickiness).  
- **Weighted Round Robin / Weighted Least Connections** – Assigns more traffic to servers with higher capacity.  
- **Random** – Random distribution across servers.  

---

## ✅ Advantages of Load Balancers  
- **High Availability** – Prevents overload by distributing requests.  
- **Scalability** – Easy to add/remove servers.  
- **Redundancy** – Failover support if a server crashes.  
- **Optimized Resource Usage** – Efficient traffic distribution.  
- **Improved User Experience** – Faster and smoother responses.  

---

## ⚡ Quick Recap  

### 🔹 Types of Load Balancers  
| **Type**        | **Example**              | **Use Case**                       |
|-----------------|--------------------------|-------------------------------------|
| **Hardware LB** | F5, Citrix Netscaler     | Data centers, large enterprises     |
| **Software LB** | Nginx, HAProxy           | Cost-effective, flexible deployments |
| **Cloud LB**    | AWS ELB, Azure LB, GCP LB| Scalable cloud applications         |

### 🔹 Load Balancing Algorithms  
| **Algorithm**   | **Working** |
|-----------------|-------------|
| **Round Robin** | Sequentially assigns requests to servers |
| **Least Connections** | Chooses server with fewer active sessions |
| **IP Hash**     | Maps client IP → fixed server (sticky sessions) |
| **Weighted**    | Distributes based on server capacity |
| **Random**      | Assigns requests randomly |

---

![Load Balancer Diagram](Assets/load-balancer.png)  

---

# THANK YOU!  
# ~ **V1NNN22** ~