# TCP Reno in Networking  
~  
## Written By: VINOD N. RATHOD.  
~  

## What is TCP Reno?  
- **Definition:** A classic TCP congestion control algorithm that manages network congestion using packet loss signals, fast retransmit, and fast recovery mechanisms.  
- **Purpose:** Prevents network collapse by reducing transmission speed when congestion is detected.  
- **Analogy:** Like a cautious driver who only slows down after noticing traffic accidents ahead instead of predicting congestion early.  

---  

## The 4 Core Steps of TCP Reno Operation  

### 1. Slow Start Phase (Step 1)  
- **Function:** TCP begins with a small congestion window and increases rapidly.  
- **Role:** Quickly discovers available bandwidth.  
- **Examples:** Congestion window doubles every RTT initially.  

---  

### 2. Congestion Avoidance (Step 2)  
- **Function:** Growth becomes linear after threshold is reached.  
- **Role:** Prevents aggressive overload.  
- **Examples:** cwnd increases incrementally over time.  

---  

### 3. Loss Detection (Step 3)  
- **Function:** Duplicate ACKs or timeout indicate packet loss.  
- **Role:** Detects congestion event.  
- **Examples:** 3 duplicate ACKs trigger fast retransmit.  

---  

### 4. Recovery Adjustment (Step 4)  
- **Function:** Congestion window is reduced and recovery begins.  
- **Role:** Stabilizes traffic after congestion.  
- **Examples:** Fast recovery avoids full restart after some losses.  

---  

## Key Features  
- **Loss-Based Control:** Reacts to packet drops.  
- **Fast Retransmit:** Resends lost packets quickly.  
- **Fast Recovery:** Avoids complete restart in some cases.  
- **Classic Design:** Foundation of later TCP algorithms.  

---  

## Why It Matters  
- **Historical Importance:** Built many TCP concepts still used today.  
- **Protocol Understanding:** Essential for learning congestion control evolution.  
- **Baseline Comparison:** Reno vs CUBIC vs BBR makes far more sense after this.  

---  

## Quick Recap (Mnemonic)  
- **Start → Avoid → Detect → Recover**  
  - **Grow → Watch → Loss → Reduce**  

---  


# THANK YOU!  
# ~ **V1NNN22**