---

# Multipath TCP (MPTCP) in Networking  
~
## Written By: VINOD N. RATHOD.  
~

## What is Multipath TCP (MPTCP)?  
- **Definition:** Multipath TCP (MPTCP) is an extension of TCP that allows a single transport-layer connection to use multiple network paths at the same time.
- **Purpose:** It improves connection reliability and can increase available throughput by using multiple interfaces or routes.
- **Analogy:** Imagine delivering one large package using two roads at once. If one road becomes blocked, the delivery can continue using the other road.

---  

## The 4 Core Steps of MPTCP Operation  

### 1. Connection Establishment  
- **Function:** The client and server establish an MPTCP-capable connection using TCP options.
- **Role:** The MP_CAPABLE option allows both endpoints to indicate support for MPTCP.
- **Examples:** A smartphone connects to a server while supporting both Wi-Fi and cellular data.

---  

### 2. Additional Path Creation  
- **Function:** MPTCP can establish additional TCP subflows over other available network paths.
- **Role:** The MP_JOIN option allows a new subflow to join the existing MPTCP connection.
- **Examples:** A phone may create one subflow over Wi-Fi and another over its cellular connection.

---  

### 3. Data Scheduling  
- **Function:** MPTCP distributes data across its available subflows according to its scheduler.
- **Role:** It can use multiple paths for throughput or reliability, depending on network conditions and implementation.
- **Examples:** Data may travel over Wi-Fi and cellular simultaneously, while the receiver reassembles the data into the original byte stream.

---  

### 4. Path Failure and Recovery  
- **Function:** If one subflow fails, MPTCP can continue sending data over another usable subflow.
- **Role:** It helps preserve the overall connection when a network interface or path becomes unavailable.
- **Examples:** If a phone leaves a Wi-Fi coverage area, its MPTCP connection may continue over cellular without restarting the application session.

---  

## Key Features  
- **Multiple Subflows:** A single connection can use multiple TCP subflows.
- **Connection Continuity:** Can survive the loss of an individual path when another path remains available.
- **Path-Level Scheduling:** Data can be distributed based on path conditions and scheduler behavior.
- **Backward Compatibility:** MPTCP can fall back to regular TCP when MPTCP support is unavailable or not negotiated.

---  

## Why It Matters  
- **Improved Reliability:** A connection can remain active during a path failure.
- **Higher Potential Throughput:** Multiple paths may contribute capacity when conditions and scheduling allow.
- **Mobile Connectivity:** Useful when devices have both Wi-Fi and cellular interfaces.
- **Network Flexibility:** Allows applications to benefit from multiple available network paths without managing each path themselves.

---  

## Quick Recap (Mnemonic)  
- **Connect → Join → Schedule → Recover**  
  - **Establish MPTCP → Add subflows → Distribute data → Continue over surviving paths**  

---  


# THANK YOU!  
# ~ **V1NNN22**