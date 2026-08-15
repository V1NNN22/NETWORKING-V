DetNet (Deterministic Networking) in Networking

~

Written By: VINOD N. RATHOD.

~

What is DetNet?

Definition: DetNet (Deterministic Networking) is a set of networking technologies designed to provide extremely predictable packet delivery with bounded latency, low packet loss, and controlled packet delay variation.

Purpose: Allows networks to carry time-sensitive traffic where packets must arrive within a predictable time limit.

Analogy: Normal networking is like a city bus that usually arrives on time. DetNet is like a train running on a reserved track with a guaranteed timetable. Humans apparently decided "approximately on time" wasn't sufficient for robots and industrial machines.



---

Why Was DetNet Created?

Problem with Traditional Networking: Normal IP networks provide best-effort delivery, so congestion can cause unpredictable delay, jitter, or packet loss.

Network Issue: Industrial robots, power grids, vehicles, and professional audio/video systems may require predictable communication.

Solution: DetNet provides mechanisms for controlling latency, packet loss, and traffic paths across a network.



---

The 4 Core Steps of DetNet Operation

1. Traffic Identification (Step 1)

Function: Time-sensitive traffic is identified and classified.

Role: Separates deterministic traffic from normal best-effort traffic.

Example: A control message for an industrial robot is classified as high-priority deterministic traffic.



---

2. Resource Reservation (Step 2)

Function: Network resources are allocated for deterministic traffic.

Role: Prevents unpredictable congestion from affecting critical packets.

Example: A specific amount of bandwidth is reserved for robot-control traffic.



---

3. Controlled Packet Forwarding (Step 3)

Function: Packets follow carefully controlled paths through the network.

Role: Keeps latency and packet loss within defined limits.

Example: Traffic is routed through a predefined path instead of dynamically changing between congested links.



---

4. Reliable Packet Delivery (Step 4)

Function: The network uses mechanisms such as packet replication and elimination when required.

Role: Improves reliability for critical traffic.

Example: A packet may travel over two independent paths, and duplicate copies are eliminated when they reach the destination.



---

Components of DetNet

1. DetNet Domain

The portion of the network providing deterministic services.

Contains routers and forwarding devices supporting DetNet functions.


2. DetNet Flow

A specific traffic flow requiring deterministic behavior.

Example: Industrial control commands.


3. Traffic Engineering

Controls how deterministic flows travel through the network.

Helps provide predictable performance.


4. Packet Replication and Elimination

Sends duplicate copies over independent paths when required.

Removes duplicates at the receiving side.



---

Real-Life Example

Suppose a factory has robotic arms controlled over a network.

Controller
    |
    v
DetNet Router
   / \
  /   \
Path A Path B
  \   /
   \ /
    v
Robot

If the control packet is extremely important:

DetNet identifies the traffic as deterministic.

Network resources are reserved.

The packet follows controlled paths.

Copies may be sent through multiple paths.

Duplicate packets are removed at the destination.

The robot receives the control message within a predictable time limit.



---

Key Features

Bounded Latency: Keeps packet delay within defined limits.

Low Packet Loss: Reduces packet loss for critical traffic.

Controlled Jitter: Helps make packet arrival times predictable.

Traffic Engineering: Controls packet paths.

Packet Replication: Can provide additional reliability.

Multi-Path Support: Can use multiple paths for protection.



---

Advantages

Predictable network performance.

Suitable for mission-critical communication.

Improved reliability.

Controlled latency and jitter.

Supports converged networks carrying critical and normal traffic.



---

Limitations

More complex than ordinary IP networking.

Requires compatible network infrastructure.

Requires careful resource planning.

Deterministic guarantees depend on proper end-to-end network design.



---

Where DetNet is Used

Industrial Automation

Robotics

Smart Grids

Autonomous Vehicles

Professional Audio/Video

Industrial IoT

5G Networks

Mission-Critical Infrastructure



---

Why It Matters

Predictability: Network behavior becomes measurable and bounded.

Reliability: Critical packets receive stronger protection.

Industrial Networking: Enables Ethernet/IP networks to support time-sensitive applications.

Convergence: Allows critical and ordinary traffic to share infrastructure while protecting deterministic flows.



---

DetNet vs Traditional IP Networking

Feature	Traditional IP	DetNet

Delivery Model	Best Effort	Deterministic
Latency	Variable	Bounded
Packet Loss	Possible	Controlled
Jitter	Variable	Controlled
Path Control	Normal Routing	Traffic Engineered
Reliability	Standard	Enhanced
Use Case	Web, Email, General Traffic	Robots, Industrial Control, Critical Systems



---

Did You Know?

DetNet can use Packet Replication and Elimination Function (PREF) techniques to send multiple copies of a packet across different paths and eliminate duplicates at the destination.

This means a network can tolerate certain path failures without requiring the application to retransmit the packet.



---

Quick Recap (Mnemonic)

Identify → Reserve → Control → Deliver

Traffic → Resources → Path → Reliability




---

THANK YOU!

~ V1NNN22