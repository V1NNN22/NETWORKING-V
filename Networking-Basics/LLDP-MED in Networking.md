---

# LLDP-MED in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is LLDP-MED?  
- **Definition:** LLDP-MED (Link Layer Discovery Protocol-Media Endpoint Discovery) is an extension of LLDP designed to provide detailed network information between network devices and media endpoints.
- **Purpose:** It helps automatically discover and configure devices such as IP phones, access points, and other endpoint equipment.
- **Analogy:** Like a building receptionist sharing the correct department, location, and emergency details with every visitor.

---  

## The 4 Core Steps of LLDP-MED Operation  

### 1. Capability Advertisement  
- **Function:** Devices advertise their LLDP-MED capabilities to neighboring devices.
- **Role:** Identifies whether a device supports features such as network policy or location information.
- **Examples:** An IP phone announces that it supports LLDP-MED network policy discovery.

---  

### 2. Device Information Exchange  
- **Function:** Devices exchange identification and capability information using LLDP frames.
- **Role:** Helps switches understand what type of endpoint is connected.
- **Examples:** A switch learns that the connected device is an IP phone rather than a regular workstation.

---  

### 3. Network Policy Delivery  
- **Function:** The switch provides configuration details to supported endpoints.
- **Role:** Allows endpoints to learn VLAN, priority, and tagging requirements automatically.
- **Examples:** An IP phone receives voice VLAN ID, Layer 2 priority, and Layer 3 DSCP settings.

---  

### 4. Endpoint Configuration and Operation  
- **Function:** The endpoint applies the received network policy.
- **Role:** Ensures voice or multimedia traffic is placed in the correct VLAN and receives suitable QoS treatment.
- **Examples:** An IP phone automatically joins the voice VLAN and marks voice traffic with the correct priority.

---  

## Key Features  
- **Automatic Discovery:** Identifies connected media endpoints.
- **Voice VLAN Assignment:** Delivers voice network policy information.
- **Location Identification:** Supports location and emergency-call information.
- **QoS Configuration:** Communicates Layer 2 and Layer 3 traffic priorities.

---  

## Why It Matters  
- **IP Telephony:** Simplifies deployment of VoIP phones.
- **Reduced Manual Configuration:** Minimizes endpoint setup effort.
- **Improved QoS:** Helps voice traffic receive appropriate priority.
- **Better Visibility:** Provides useful endpoint and location details.

---  

## Quick Recap (Mnemonic)  
- **C → E → P → A**  
  - **Capabilities → Exchange → Policy → Apply Configuration**  

---  


# THANK YOU!  
# ~ **V1NNN22**