BGP Add-Path in Networking

~

Written By: VINOD N. RATHOD.

~

What is BGP Add-Path?

Definition: BGP Add-Path is a BGP extension that allows a router to advertise multiple paths for the same destination prefix instead of advertising only its single best path.

Purpose: Improves routing diversity, faster convergence, and traffic engineering by allowing multiple valid paths to be shared with BGP neighbors.

Analogy: Imagine Google Maps showing you only one route to a destination. Normal BGP does something similar. Add-Path lets the router say, "Here are several good routes. Keep the alternatives ready."



---

Why Was BGP Add-Path Created?

Problem with Traditional BGP: A BGP router normally advertises only its selected best path for a prefix.

Network Issue: Other routers may never learn about alternative paths that could be useful if the best path fails.

Solution: Add-Path allows multiple paths for the same prefix to be advertised to a BGP neighbor.



---

The 4 Core Steps of BGP Add-Path Operation

1. Multiple Path Learning (Step 1)

Function: A router learns multiple valid BGP paths for the same prefix.

Role: Keeps alternative routing information available.

Example: Router A learns three paths to 10.10.10.0/24.



---

2. Best Path Selection (Step 2)

Function: BGP still selects its preferred path using the normal BGP decision process.

Role: Determines the primary route.

Example: Path through ISP-A is selected as the best path.



---

3. Multiple Path Advertisement (Step 3)

Function: With Add-Path enabled, the router advertises multiple paths to its BGP neighbor.

Role: Gives the neighboring router additional routing choices.

Example: Router A advertises paths through ISP-A, ISP-B, and ISP-C.



---

4. Alternative Path Utilization (Step 4)

Function: The receiving router stores the additional paths and can use them when required.

Role: Improves convergence and enables better traffic engineering.

Example: If the primary ISP-A path fails, the router already knows about the ISP-B path.



---

Components of BGP Add-Path

1. Multiple BGP Paths

Several valid paths can exist for the same prefix.

Not all paths need to be selected as the best path.


2. Path Identifier (Path ID)

Uniquely identifies an advertised path.

Helps the receiver distinguish multiple paths for the same prefix.


3. BGP Speaker

Learns and advertises multiple paths.

Controls how many paths are shared.


4. BGP Neighbor

Receives multiple paths when the Add-Path capability is negotiated.

Stores the additional routing information.



---

Real-Life Example

Suppose an ISP has three possible routes to the same destination:

┌── ISP-A ── Best Path
                 │
Router A ────────┼── ISP-B ── Backup
                 │
                 └── ISP-C ── Backup

Normal BGP:

Router A selects ISP-A.

Only the best path is normally advertised.

ISP-B and ISP-C may remain hidden from the neighbor.


BGP Add-Path:

Router A can advertise multiple paths.

The neighbor learns ISP-A, ISP-B, and ISP-C.

If ISP-A fails, alternative paths are already known.



---

Key Features

Multiple Path Advertisement: Advertises several paths for the same prefix.

Path Identification: Uses Path IDs to distinguish different paths.

Faster Convergence: Alternative paths can already be available.

Traffic Engineering: Provides more routing choices.

Improved Route Diversity: Prevents useful alternative paths from being hidden.



---

Advantages

Faster recovery after failures.

Improves routing diversity.

Enables better traffic engineering.

Reduces dependence on a single advertised path.

Useful in large service-provider networks.



---

Limitations

Increases BGP update traffic.

Requires additional memory for storing paths.

Requires support on both BGP peers.

Can increase routing complexity.

Multiple advertised paths do not automatically mean all paths are used for forwarding.



---

Where BGP Add-Path is Used

Internet Service Providers (ISPs)

Large Enterprise Networks

Data Center Networks

MPLS Networks

Cloud Provider Networks

Route Reflector Architectures

Multi-Homed Networks



---

Why It Matters

Path Diversity: Routers can learn multiple alternatives.

Fast Recovery: Backup routes can already be available.

Traffic Engineering: Operators gain greater control over route selection.

Scalability: Helps when traditional BGP hides useful alternative paths.

Reliability: Reduces dependence on a single advertised route.



---

BGP vs BGP Add-Path

Feature	Traditional BGP	BGP Add-Path

Paths Advertised	Usually one best path	Multiple paths
Alternative Paths	Often hidden from neighbor	Can be advertised
Path Diversity	Lower	Higher
Convergence	May require new path learning	Alternatives may already exist
Traffic Engineering	More limited	More flexible
BGP Updates	Lower	Higher



---

Did You Know?

BGP Add-Path does not mean BGP installs every advertised path into the forwarding table.

Its main purpose is to allow multiple paths to be advertised and learned.

The receiving router still applies its own BGP decision process and forwarding policies.



---

Quick Recap (Mnemonic)

Learn → Select → Advertise → Backup

Paths → Best → Multiple → Recovery




---

THANK YOU!

~ V1NNN22