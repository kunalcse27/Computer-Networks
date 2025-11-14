1️⃣ Step 1: Install Nmap
On Windows:

Go to the official Nmap website.

Download the installer (e.g., nmap-<version>-setup.exe).

Run the installer → keep default settings.

This installs both:

Nmap (command-line tool)

Zenmap (GUI tool)

2️⃣ Step 2: Open Nmap / Zenmap

You can use either:

✔ Command Prompt

Open CMD → type:

nmap


OR

✔ Zenmap (GUI version)

Go to Start Menu → search “Zenmap” → open it.

🟦 NOW START USING NMAP FEATURES
3️⃣ Step 3: Find Live Hosts (Ping Sweep)

This scan shows which devices are powered on in the network.

Example (replace with your network):

nmap -sn 192.168.1.0/24


You will get:

Active devices

Their IP addresses

MAC addresses

4️⃣ Step 4: Perform Basic Host Scan

To scan a single computer:

nmap 192.168.1.5


You will get:

Open ports

Services running

Host status

5️⃣ Step 5: List Scan (No packets sent)
nmap -sL 192.168.1.0/24


Shows list of hosts without scanning them.

6️⃣ Step 6: Scan for Open Ports
TCP SYN Scan:
nmap -sS 192.168.1.5

UDP Scan:
nmap -sU 192.168.1.5

7️⃣ Step 7: Study Different Ping Types
Disable ARP ping:
nmap -sn 192.168.1.5 --disable-arp-ping

TCP SYN ping:
nmap -PS 192.168.1.5

TCP ACK ping:
nmap -PA 192.168.1.5

ICMP ping:
nmap -PE 192.168.1.5

8️⃣ Step 8: ARP Ping Scan (Local Network Detection)
nmap -PR 192.168.1.0/24

9️⃣ Step 9: OS Detection
Basic OS detection:
nmap -O 192.168.1.5

Aggressive OS detection:
nmap -A 192.168.1.5


This gives:

OS guess

Services & versions

Traceroute

Scripts results

🔟 Step 10: TCP Window Scan
nmap -sW 192.168.1.5


Shows:

Active ports

TCP window sizes

1️⃣1️⃣ Step 11: Use Timing Templates

Fast scan (for LAN):

nmap -T4 192.168.1.0/24


Slow / stealthy scan:

nmap -T1 192.168.1.0/24

1️⃣2️⃣ Step 12: Save Scan Results (Logging)

Save scan output to all formats:

nmap -oA myscan 192.168.1.5


This creates:

myscan.nmap

myscan.gnmap

myscan.xml

🎉 CONCLUSION (Ready-made)

Thus, we successfully installed Nmap and performed various scans such as host discovery, port scanning, OS detection, ARP ping, TCP/UDP ping, and aggressive scanning. This experiment helps network administrators and security analysts discover hosts, open ports, network vulnerabilities, firewall behavior, and operating systems in the network.
