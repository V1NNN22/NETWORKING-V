# BBRv2 (Bottleneck Bandwidth and Round-trip propagation time Version 2) in Networking
~
## Written By: VINOD N. RATHOD.
~

## What is BBRv2?
- **Definition:** BBRv2 is an evolution of the BBR congestion-control algorithm that uses a model of bottleneck bandwidth, round-trip propagation time, and network congestion signals to control TCP sending behavior.
- **Purpose:** Improves fairness, congestion response, and coexistence with other traffic while maintaining high throughput and low latency.
- **Analogy:** BBRv1 is like a driver estimating road capacity and speed. BBRv2 adds information about how crowded the road is, allowing the driver to avoid taking more space than necessary.

---

## The 4 Core Steps of BBRv2 Operation

### 1. Network Model Estimation (Step 1)
- **Function:** BBRv2 estimates bottleneck bandwidth and the minimum round-trip propagation time.
- **Role:** Builds an internal model of the network path.
- **Examples:** Measuring delivered bandwidth and tracking the minimum observed RTT.

---

### 2. Congestion Detection (Step 2)
- **Function:** BBRv2 monitors congestion-related signals such as ECN markings, packet loss, and increasing queues.
- **Role:** Detects when the network is becoming congested.
- **Examples:** Responding to ECN marks before severe packet loss occurs.

---

### 3. Sending Rate Control (Step 3)
- **Function:** BBRv2 adjusts pacing rate and congestion window based on its network model.
- **Role:** Controls how much traffic enters the network.
- **Examples:** Reducing the sending rate when congestion becomes significant.

---

### 4. Continuous Probing (Step 4)
- **Function:** BBRv2 periodically probes the network to determine whether additional bandwidth is available.
- **Role:** Maintains high utilization while attempting to avoid excessive queue buildup.
- **Examples:** Increasing the pacing rate temporarily to test whether the bottleneck can handle more traffic.

---

## Key Features
- **Model-Based Control:** Uses bandwidth and RTT measurements.
- **Congestion Awareness:** Considers loss and ECN signals.
- **Improved Fairness:** Designed to coexist better with other congestion-control algorithms.
- **Low Latency:** Attempts to prevent excessive queue buildup.
- **Adaptive Pacing:** Continuously changes transmission behavior according to network conditions.

---

## Why It Matters
- **Better Congestion Control:** Reacts to more than just packet loss.
- **Fairness:** Designed to improve coexistence with competing flows.
- **High Throughput:** Continues probing for available capacity.
- **Lower Queueing Delay:** Attempts to avoid persistent excessive queues.
- **Modern Networks:** Useful for high-speed and variable network environments.

---

## Quick Recap (Mnemonic)
- **Model → Detect → Control → Probe**
  - **Bandwidth → Congestion → Rate → Capacity**

---


# THANK YOU!
# ~ **V1NNN22**