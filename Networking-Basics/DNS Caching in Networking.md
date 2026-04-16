# DNS Caching in Networking  
~
## Written By: VINOD N. RATHOD.  
~

## What is DNS Caching?  
- **Definition:** A mechanism where DNS query results (domain → IP mappings) are stored temporarily to speed up future lookups.  
- **Purpose:** Reduces DNS query time and network load → improves browsing performance.  
- **Analogy:** Like remembering a frequently dialed phone number instead of checking the contact list every time.  

---

## The 4 Core Steps of DNS Caching  

### 1. Initial Query (Step 1)  
- **Function:** Client requests IP for a domain.  
- **Role:** If not cached, query goes through full DNS resolution.  
- **Examples:** First-time visit to a website.  

---

### 2. Response Storage (Step 2)  
- **Function:** DNS resolver stores the result locally.  
- **Role:** Saves domain-IP mapping for reuse.  
- **Examples:** Browser or OS DNS cache.  

---

### 3. Cache Hit (Step 3)  
- **Function:** Future requests served from cache.  
- **Role:** Skips full DNS lookup process.  
- **Examples:** Faster access to frequently visited sites.  

---

### 4. Cache Expiry (Step 4)  
- **Function:** Cached entry expires after TTL (Time-To-Live).  
- **Role:** Ensures updated IP is fetched when needed.  
- **Examples:** TTL value defined in DNS records.  

---

## Types of DNS Caching  
- **Browser Cache:** Stored in web browser.  
- **OS Cache:** Stored in operating system.  
- **Resolver Cache:** Stored in ISP DNS servers.  

---

## Why It Matters  
- **Performance:** Speeds up domain resolution.  
- **Reduced Load:** Decreases DNS server queries.  
- **Efficiency:** Improves overall network experience.  

---

## Quick Recap (Mnemonic)  
- **Query → Store → Use → Expire**  
  - **Request → Cache → Fast Access → TTL**  

---

# THANK YOU!  
# ~ **V1NNN22**