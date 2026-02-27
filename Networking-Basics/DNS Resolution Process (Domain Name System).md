# DNS Resolution Process (Domain Name System)  
~
## Written By: VINOD N. RATHOD.  
~

## What is DNS Resolution?  
- **Definition:** A process that translates human-readable domain names into machine-readable IP addresses.  
- **Purpose:** Allows users to access websites using names instead of numerical IP addresses → simplifies internet usage and routing.  
- **Analogy:** Like a phone contact list, where a name is mapped to a phone number.  

---

## The 7 Steps of DNS Resolution  

### 1. User Request (Step 1)  
- **Function:** User enters a domain name in the browser.  
- **Role:** Initiates DNS lookup query.  
- **Examples:** Typing `example.com` in Chrome.  

---

### 2. Browser Cache Check (Step 2)  
- **Function:** Browser checks if it already knows the IP.  
- **Role:** Reduces latency and avoids external queries.  
- **Examples:** Previously visited websites.  

---

### 3. OS Cache Check (Step 3)  
- **Function:** Operating system checks its local DNS cache.  
- **Role:** Stores recent domain → IP mappings.  
- **Examples:** `ipconfig /displaydns` (Windows).  

---

### 4. Resolver Query (Step 4)  
- **Function:** Request sent to recursive DNS resolver.  
- **Role:** Resolver handles lookup on behalf of user.  
- **Examples:** ISP DNS server, Google DNS (8.8.8.8).  

---

### 5. Root Server Query (Step 5)  
- **Function:** Resolver asks root server where TLD server is.  
- **Role:** Directs query to correct domain extension authority.  
- **Examples:** `.com`, `.org`, `.net` root zones.  

---

### 6. TLD Server Query (Step 6)  
- **Function:** TLD server returns authoritative name server.  
- **Role:** Points resolver to actual domain record holder.  
- **Examples:** `.com` registry servers.  

---

### 7. Authoritative Server Response (Step 7)  
- **Function:** Returns final IP address of domain.  
- **Role:** Completes resolution process.  
- **Examples:** Domain hosting provider DNS records.  

---

## Quick Recap (Mnemonic)  
- **User Browsers Often Require Root To Answer**  
  - **User → Browser → OS → Resolver → Root → TLD → Authoritative**  

---

![Diagram](Assets/dns.webp)  

---

# THANK YOU!  
# ~ **V1NNN22**