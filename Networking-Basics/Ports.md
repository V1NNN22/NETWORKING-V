# Port Numbers (Well-known, Registered, Dynamic)  
~
## Written By: VINOD N. RATHOD.  
~

## What is a Port Number?  
- **Definition:** A port number is a 16-bit numerical value used to identify specific processes or services on a device within a network.  
- **Purpose:** Allows multiple applications/services to share a single IP address by distinguishing their network traffic.  
- **Layer:** Operates at the Transport Layer (Layer 4) of the OSI model (used by TCP and UDP).  

---

## Range of Port Numbers (0–65,535)  
- **Total available ports:** 65,536 (from 0 to 65,535).  
- **Divided into categories:** Assigned and maintained by **IANA (Internet Assigned Numbers Authority).**  

---

## Types of Port Numbers  

### 1. Well-known Ports (0–1023)  
- **Reserved for:** Standard and widely used services.  
- **Examples:**  
  - Port 20/21 → FTP (File Transfer Protocol)  
  - Port 22 → SSH (Secure Shell)  
  - Port 25 → SMTP (Simple Mail Transfer Protocol)  
  - Port 53 → DNS (Domain Name System)  
  - Port 80 → HTTP (Web traffic)  
  - Port 443 → HTTPS (Secure web traffic)  

---

### 2. Registered Ports (1024–49,151)  
- **Assigned to:** Specific user processes or applications by IANA.  
- **Usage:** Commonly used by vendors for proprietary applications.  
- **Examples:**  
  - Port 3306 → MySQL Database  
  - Port 3389 → Microsoft RDP (Remote Desktop Protocol)  

---

### 3. Dynamic / Private / Ephemeral Ports (49,152–65,535)  
- **Assigned:** Not permanent, allocated dynamically.  
- **Usage:** Temporary connections (mainly client-side communication).  
- **Example:** When you open a web browser, your PC uses a random port in this range to connect to a server (e.g., to port 80/443).  

---

![Diagram](Assets/ports.png)  

---

## Quick Recap  
- **Well-known:** 0–1023 → Standard services.  
- **Registered:** 1024–49,151 → Vendor/user applications.  
- **Dynamic:** 49,152–65,535 → Temporary/ephemeral client ports.  

---

# THANK YOU!  
# ~ **V1NNN22**  
