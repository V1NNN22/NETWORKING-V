# Networking Basics & Key Terminology
~
## Written By: VINOD N. RATHOD.
~

## Communication Types: Unicast, Broadcast, Multicast, Anycast  

### Unicast  
- **Definition:** Communication between one sender and one receiver.  
- **How it works:** Data is sent directly from one device to another specific device.  
- **Examples:**  
  - Browsing a website (your computer → specific server).  
  - Sending an email to one person.  
- **Key Point:** One-to-one communication.  

---

### Broadcast  
- **Definition:** Communication between one sender and all devices in the network.  
- **How it works:** The message is sent to everyone on the same network segment.  
- **Examples:**  
  - Sending ARP (Address Resolution Protocol) requests in a LAN.  
  - Radio or TV broadcast signals.  
- **Key Point:** One-to-all communication.  

---

### Multicast  
- **Definition:** Communication between one sender and a selected group of receivers.  
- **How it works:** The message is sent only to devices that have “joined” the multicast group.  
- **Examples:**  
  - Online video streaming (live sports sent only to subscribers).  
  - Video conferencing for selected participants.  
- **Key Point:** One-to-many (but not all) communication.  

---

### Anycast  
- **Definition:** Communication between one sender and the nearest/most optimal receiver out of many possible receivers.  
- **How it works:** The network decides which receiver (out of many) is closest or most efficient to respond.  
- **Examples:**  
  - DNS (Domain Name System) queries — your request is answered by the nearest DNS server.  
  - Content Delivery Networks (CDNs) like Cloudflare or Akamai deliver content from the closest server.  
- **Key Point:** One-to-nearest/optimal communication.  

---

## Quick Comparison  
- **Unicast** → One sender → One receiver (direct communication)  
- **Broadcast** → One sender → All receivers (everyone gets it)  
- **Multicast** → One sender → Selected group of receivers (chosen group only)  
- **Anycast** → One sender → Nearest/most efficient receiver (network decides)  

---
# THANK YOU!  
# ~ **V1NNN22** ~
