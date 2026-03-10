# Port Numbers in Networking  
~
## Written By: VINOD N. RATHOD.  
~

## What are Port Numbers?  
- **Definition:** Numerical identifiers used by transport layer protocols to distinguish between different services running on the same device.  
- **Purpose:** Allows multiple network services to operate simultaneously on one IP address.  
- **Analogy:** Like apartment numbers in a building where the building address is the IP and each apartment is a port.  

---

## The 4 Core Port Number Categories  

### 1. Well-Known Ports (0–1023)  
- **Function:** Reserved for common system services.  
- **Role:** Used by standard protocols.  
- **Examples:**  
  - HTTP → Port 80  
  - HTTPS → Port 443  
  - FTP → Port 21  
  - SSH → Port 22  

---

### 2. Registered Ports (1024–49151)  
- **Function:** Assigned to specific services by organizations.  
- **Role:** Used by user-level applications.  
- **Examples:**  
  - MySQL → Port 3306  
  - PostgreSQL → Port 5432  

---

### 3. Dynamic / Ephemeral Ports (49152–65535)  
- **Function:** Temporary ports assigned by operating systems.  
- **Role:** Used for client-side communication sessions.  
- **Examples:** Browser opening temporary ports to access websites.  

---

### 4. Port Communication Process  
- **Function:** Enables applications to communicate over network using TCP or UDP.  
- **Role:** Source port identifies sender process, destination port identifies receiving service.  
- **Examples:** Browser → HTTPS server communication.  

---

## Key Concepts  
- **Source Port:** Identifies sending application.  
- **Destination Port:** Identifies receiving service.  
- **TCP/UDP Ports:** Both protocols use port numbers for communication.  

---

## Why It Matters  
- **Service Identification:** Directs network traffic to correct application.  
- **Security:** Firewalls filter traffic based on ports.  
- **Multiplexing:** Multiple services run on a single host simultaneously.  

---

## Quick Recap (Mnemonic)  
- **System → Service → Session → Communication**  
  - **Well-Known → Registered → Dynamic → Transport**  

---


# THANK YOU!  
# ~ **V1NNN22**