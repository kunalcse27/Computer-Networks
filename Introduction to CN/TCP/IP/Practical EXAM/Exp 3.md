1️⃣ Step 1: Install and Open Wireshark

Download Wireshark from its official website.

Install it with default settings.

Open Wireshark.

You will see a list of network interfaces (WiFi, Ethernet, etc.).

2️⃣ Step 2: Start Packet Capture

Click on your active network interface (usually Wi-Fi).

Wireshark will start capturing packets in real time.

Packets will begin to appear in the top window.

3️⃣ Step 3: Verify Promiscuous Mode

Go to Capture → Options

Ensure “Enable promiscuous mode on all interfaces” is checked.
(This allows Wireshark to capture all packets on the network.)

4️⃣ Step 4: Generate Network Traffic

To see different protocol packets:

Try doing:

Open google.com → generates DNS, TCP, HTTP

Ping a website → generates ICMP

Refresh a webpage → more TCP packets

This lets you capture packets from many layers.

5️⃣ Step 5: Stop the Capture

After 10–20 seconds, click the Red Stop button on the top-left.

⭐ NOW START ANALYSING DIFFERENT TCP/IP LAYERS
6️⃣ Step 6: Study Ethernet Layer (Frame Header, Frame Size)

Click any packet.

In the middle pane, expand "Ethernet II".

Note:

Source MAC address

Destination MAC address

Type

Frame length

7️⃣ Step 7: Study Data Link Layer (MAC, ARP)

In filter bar type:

arp


and press Enter

Select an ARP packet.

Observe:

Sender MAC

Sender IP

Target MAC

Target IP
This shows IP ↔ MAC binding.

8️⃣ Step 8: Study Network Layer (IP, ICMP)
A. For IP packets

Apply filter:

ip


Select an IP packet → expand "Internet Protocol Version 4".

Observe:

IP header

Source/destination IP

TTL

Fragmentation fields

B. For ICMP packets

Type:

icmp


Find "Echo (ping) request/reply" packets.

Observe:

Type (8 = request, 0 = reply)

Code

Checksum

9️⃣ Step 9: Study Transport Layer (TCP Handshake, Ports)
A. Filter TCP packets
tcp

B. Look for TCP handshake

Find packets with:

SYN

SYN, ACK

ACK

C. Observe

Source port

Destination port

Sequence number

Acknowledgment number

🔟 Step 10: Study Application Layer (HTTP, FTP, DHCP)
A. HTTP

Filter:

http


Look for:

GET

POST

HTTP headers

B. DHCP
dhcp


Observe DHCP Discover, Offer, Request, Ack.

C. FTP
ftp


Observe login commands, file transfers (if available).

🔵 OPTIONAL BUT IMPORTANT FEATURES
11️⃣ Step 11: Use “Follow TCP Stream”

Right-click any TCP packet → Follow → TCP Stream

View full conversation between client & server.

12️⃣ Step 12: Apply Filters

Try:

dns

icmp

tcp.port==80

ip.addr == your_IP

13️⃣ Step 13: Save the Capture

Go to File → Save As

Save in .pcapng format.

✅ CONCLUSION

You have successfully:

Captured live packets

Learned how to analyze various TCP/IP layers

Observed Ethernet, ARP, IP, ICMP, TCP, and HTTP packets

Used Wireshark filters and packet inspection tools
