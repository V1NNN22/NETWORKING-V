# Reverse ARP (RARP) in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is RARP?  
- **Definition:** Reverse ARP (RARP) allows a device to discover its own IP address using its MAC address.  
- **Purpose:** Used by diskless systems during boot.  
- **Simple Meaning:** Device asks, “I know my MAC, what is my IP?”  

---  

## The 4 Core Steps of RARP  

### 1. Device Boot (Step 1)  
- **Function:** Device starts without knowing its IP.  
- **Example:** Diskless workstation startup.  

---  

### 2. RARP Broadcast (Step 2)  
- **Function:** Device broadcasts MAC address request.  
- **Example:** `My MAC is AA:BB:CC, what is my IP?`  

---  

### 3. RARP Server Reply (Step 3)  
- **Function:** RARP server matches MAC with configured IP.  
- **Role:** Sends assigned IP address.  

---  

### 4. Network Communication (Step 4)  
- **Function:** Device uses received IP for communication.  
- **Result:** System joins network.  

---  

## Why RARP Exists  
- **Old diskless systems**  
- **Bootstrapping network devices**  
- **Early IP assignment method**  

---  

## Real-World Problems  
- **Requires dedicated RARP server**  
- **Limited functionality**  
- **No subnet/gateway info**  
- **Obsolete technology**  

---  

## Modern Replacement  
- **BOOTP**  
- **DHCP**  

These provide:  
- IP address  
- Subnet mask  
- Gateway  
- DNS  

---  

## Detection  
```bash
tcpdump -i any rarp
```

Check:  
- RARP request/reply packets  

---  

## Key Features  
- MAC to IP mapping  
- Boot-time IP discovery  
- Legacy protocol  
- Replaced by DHCP  

---  

## Why It Matters  
- **Networking history**  
- **Protocol evolution understanding**  
- **Useful in legacy environment analysis**  

---  

## Quick Recap  
**Boot → Ask → Server Reply → Join Network**  
**MAC → RARP → IP → Connect**  

---  

# THANK YOU!  
# ~ **V1NNN22**