---

# Root Guard in Spanning Tree Protocol  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is Root Guard?  
- **Definition:** A Layer 2 security feature used with Spanning Tree Protocol (STP) to prevent an unauthorized switch from becoming the STP Root Bridge.  
- **Purpose:** Protects the intended STP topology by restricting superior BPDU information received on protected ports.  
- **Analogy:** Like giving one person permanent authority over a meeting and preventing an unexpected attendee from suddenly becoming the chairperson.  

---  

## The 4 Core Steps of Root Guard Operation  

### 1. Port Protection (Step 1)  
- **Function:** Root Guard is enabled on selected switch ports where the STP root should not be learned from.  
- **Role:** Establishes a boundary for where the Root Bridge can legitimately exist.  
- **Examples:** Root Guard is commonly configured toward downstream switches or untrusted Layer 2 connections.  

---  

### 2. BPDU Monitoring (Step 2)  
- **Function:** The protected port continuously examines incoming BPDUs.  
- **Role:** Determines whether another switch is advertising a superior STP path to the current Root Bridge.  
- **Examples:** A downstream switch sends a BPDU with a better Bridge ID than the expected Root Bridge.  

---  

### 3. Root-Inconsistent State (Step 3)  
- **Function:** If a superior BPDU is received, the protected port is placed into a root-inconsistent state.  
- **Role:** Prevents the unauthorized switch from influencing the STP root election.  
- **Examples:** The port stops forwarding normal traffic while the superior BPDU condition exists.  

---  

### 4. Automatic Recovery (Step 4)  
- **Function:** Once the superior BPDU condition disappears, the port can automatically recover.  
- **Role:** Restores normal STP operation without requiring manual intervention.  
- **Examples:** Removing the unauthorized switch causes the protected port to return to its normal STP state.  

---  

## Key Features  
- **Root Protection:** Prevents unexpected Root Bridge changes.  
- **BPDU-Based:** Reacts specifically to superior BPDU information.  
- **Automatic Recovery:** Port can recover after the condition disappears.  
- **Topology Control:** Helps maintain the intended STP hierarchy.  

---  

## Why It Matters  
- **Network Stability:** Prevents accidental changes to the STP topology.  
- **Performance:** Avoids unexpected traffic paths caused by an unwanted Root Bridge.  
- **Security:** Limits the ability of unauthorized switches to influence STP elections.  
- **Operational Control:** Keeps the intended core or distribution switch as the STP Root Bridge.  

---  

## Quick Recap (Mnemonic)  
- **Protect → Monitor → Block → Recover**  
  - **Port → BPDU → Root Election → Normal State**  

---  


# THANK YOU!  
# ~ **V1NNN22**