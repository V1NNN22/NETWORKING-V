# Caching in Networking  
~
## Written By: VINOD N. RATHOD.  
~

## What is Caching?  
- **Definition:** A technique of storing frequently accessed data temporarily to reduce access time and improve performance.  
- **Purpose:** Minimizes repeated data fetching from original source → speeds up response and reduces load.  
- **Analogy:** Like keeping frequently used files on your desk instead of going to the storage room every time.  

---

## The 4 Core Steps of Caching  

### 1. Initial Request (Step 1)  
- **Function:** Client requests data from server.  
- **Role:** If cache is empty, request goes to origin server.  
- **Examples:** First-time website visit.  

---

### 2. Data Storage (Step 2)  
- **Function:** Server response is stored in cache.  
- **Role:** Saves data for future requests.  
- **Examples:** Browser caching images or HTML.  

---

### 3. Cache Hit (Step 3)  
- **Function:** Subsequent requests served from cache.  
- **Role:** Reduces latency and server load.  
- **Examples:** Reloading webpage loads faster.  

---

### 4. Cache Expiry (Step 4)  
- **Function:** Cached data expires or gets invalidated.  
- **Role:** Ensures updated content is fetched when needed.  
- **Examples:** TTL (Time-To-Live) expiration.  

---

## Types of Caching  
- **Browser Cache:** Stored on user device.  
- **Proxy Cache:** Stored in intermediary servers.  
- **CDN Cache:** Stored in edge servers globally.  
- **Server Cache:** Stored at application/server level.  

---

## Why It Matters  
- **Performance:** Faster response times.  
- **Efficiency:** Reduces server load.  
- **Scalability:** Handles high traffic effectively.  

---

## Quick Recap (Mnemonic)  
- **Request → Store → Serve → Expire**  
  - **Miss → Cache → Hit → Refresh**  

---

# THANK YOU!  
# ~ **V1NNN22**