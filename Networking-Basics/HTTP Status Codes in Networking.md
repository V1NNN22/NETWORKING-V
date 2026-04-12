# HTTP Status Codes in Networking  
~
## Written By: VINOD N. RATHOD.  
~

## What are HTTP Status Codes?  
- **Definition:** Standard response codes returned by a server to indicate the result of a client’s request.  
- **Purpose:** Helps client understand whether request was successful, failed, or needs further action.  
- **Analogy:** Like exam results showing pass, fail, or retry.  

---

## The 5 Classes of HTTP Status Codes  

### 1. 1xx – Informational (Step 1)  
- **Function:** Indicates request received and processing continues.  
- **Role:** Temporary response before final result.  
- **Examples:** 100 Continue.  

---

### 2. 2xx – Success (Step 2)  
- **Function:** Request successfully processed.  
- **Role:** Indicates everything worked correctly.  
- **Examples:** 200 OK, 201 Created.  

---

### 3. 3xx – Redirection (Step 3)  
- **Function:** Further action required to complete request.  
- **Role:** Redirects client to another resource.  
- **Examples:** 301 Moved Permanently, 302 Found.  

---

### 4. 4xx – Client Errors (Step 4)  
- **Function:** Error due to client-side issue.  
- **Role:** Indicates invalid request or unauthorized access.  
- **Examples:** 400 Bad Request, 401 Unauthorized, 404 Not Found.  

---

### 5. 5xx – Server Errors (Step 5)  
- **Function:** Error due to server-side issue.  
- **Role:** Indicates server failed to fulfill request.  
- **Examples:** 500 Internal Server Error, 503 Service Unavailable.  

---

## Why It Matters  
- **Debugging:** Helps identify issues quickly.  
- **API Development:** Essential for proper communication.  
- **User Experience:** Guides client behavior based on response.  

---

## Quick Recap (Mnemonic)  
- **Info → Success → Redirect → Client → Server**  
  - **1xx → 2xx → 3xx → 4xx → 5xx**  

---

# THANK YOU!  
# ~ **V1NNN22**