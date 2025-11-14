Step 1: Open Cisco Packet Tracer

Launch Packet Tracer from your PC.

You will see a blank workspace (canvas).

2️⃣ Step 2: Create the Network Topology
✔ Build a simple topology (Star or Router-based)

You can choose one of these two basic designs:

A. Star Topology using Hub / Switch (Beginner level)

OR

B. Static Routing Topology using 2 Routers + PCs (Required for AIM)

Below is the procedure for static routing, since your AIM includes static routing protocol.

⭐ STATIC ROUTING TOPOLOGY (REQUIRED)
3️⃣ Step 3: Place the Network Devices

From the Devices menu:

Go to Network Devices → Routers

Drag 2 routers onto the workspace.

Go to Network Devices → Switches

Drag 2 switches (one for each router).

Go to End Devices → PC

Drag 2 PCs for each router (total 4 PCs).

Your diagram now has:

Router1 → Switch1 → PC1, PC2

Router2 → Switch2 → PC3, PC4

Router1 ↔ Router2 (direct serial or copper connection)

4️⃣ Step 4: Connect the Devices

Use Connections → Copper Straight-Through:

PC → Switch (FastEthernet)

Switch → Router (FastEthernet)

Use Connections → Copper Crossover:

Router1 → Router2 (GigabitEthernet to GigabitEthernet)

⭐ CONFIGURE IP ADDRESSES
5️⃣ Step 5: Assign IP Addresses to PCs

Click each PC:

Go to Desktop → IP Configuration

Enter the IP, subnet mask, and gateway.

Example addressing plan:
Device	IP Address	Subnet Mask	Default Gateway
PC1	192.168.1.10	255.255.255.0	192.168.1.1
PC2	192.168.1.11	255.255.255.0	192.168.1.1
PC3	192.168.2.10	255.255.255.0	192.168.2.1
PC4	192.168.2.11	255.255.255.0	192.168.2.1
6️⃣ Step 6: Configure Router Interfaces
For Router1:

Click Router1 → CLI

Type:

enable
configure terminal
interface gigabitEthernet 0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit

interface gigabitEthernet 0/1
ip address 10.0.0.1 255.255.255.0
no shutdown
exit

For Router2:
enable
configure terminal
interface gigabitEthernet 0/0
ip address 192.168.2.1 255.255.255.0
no shutdown
exit

interface gigabitEthernet 0/1
ip address 10.0.0.2 255.255.255.0
no shutdown


Now both routers share a common network: 10.0.0.0/24

⭐ CONFIGURE STATIC ROUTING
7️⃣ Step 7: Add Static Routes on Both Routers
On Router1 (to reach Router2 LAN 192.168.2.0):
ip route 192.168.2.0 255.255.255.0 10.0.0.2

On Router2 (to reach Router1 LAN 192.168.1.0):
ip route 192.168.1.0 255.255.255.0 10.0.0.1


Now both routers know how to reach each other’s networks.

⭐ TEST THE NETWORK
8️⃣ Step 8: Test Connectivity
A. Using Ping

Click PC1 → Desktop → Command Prompt

Type:

ping 192.168.2.10


If the static routing works, the ping will succeed.

9️⃣ Step 9: Use Simple PDU Tool (Graphical Test)

Click Add Simple PDU (envelope icon).

Click PC1 → PC3.

Go to Simulation Mode to watch the packet move across the network.

🎉 CONCLUSION (Write This)

Hence, we successfully created a simple network topology in Cisco Packet Tracer, assigned IP addresses with subnetting and masking, connected routers using static routing protocol, and verified communication between different networks.
