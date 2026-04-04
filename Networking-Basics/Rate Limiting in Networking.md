# Rate Limiting in Networking  
~
## Written By: VINOD N. RATHOD.  
~

## What is Rate Limiting?  
- **Definition:** A technique used to control the number of requests a client can make to a server within a specific time period.  
- **Purpose:** Prevents abuse, protects servers from overload, and ensures fair usage of resources.  
- **Analogy:** Like limiting how many times a person can enter a store in a day to avoid overcrowding.  

---

## The 4 Core Steps of Rate Limiting  

### 1. Request Tracking (Step 1)  
- **Function:** Server tracks incoming requests from a client.  
- **Role:** Identifies user via IP, API key, or session.  
- **Examples:** Counting requests per minute per user.  

---

### 2. Limit Definition (Step 2)  
- **Function:** Set maximum allowed requests within time window.  
- **Role:** Defines threshold for acceptable usage.  
- **Examples:** 100 requests per minute.  

---

### 3. Enforcement (Step 3)  
- **Function:** Server checks if request exceeds limit.  
- **Role:** Allows or blocks request accordingly.  
- **Examples:** Returning HTTP 429 Too Many Requests.  

---

### 4. Reset Mechanism (Step 4)  
- **Function:** Counter resets after time window expires.  
- **Role:** Allows new set of requests.  
- **Examples:** Limit resets every minute/hour.  

---

## Common Algorithms  
- **Fixed Window:** Simple counting per time window.  
- **Sliding Window:** More accurate request tracking.  
- **Token Bucket:** Allows bursts within limits.  
- **Leaky Bucket:** Smoothens traffic flow.  

---

## Why It Matters  
- **Security:** Prevents brute-force and DDoS attacks.  
- **Performance:** Protects server from overload.  
- **Fair Usage:** Ensures equal access for all users.  

---

## Quick Recap (Mnemonic)  
- **Track → Limit → Enforce → Reset**  
  - **Count → Threshold → Block/Allow → Refresh**  

---


# THANK YOU!  
# ~ **V1NNN22**