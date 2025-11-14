STEP-WISE COMMANDS
1️⃣ PING
Purpose: Check connectivity to another device/website.
Steps

In CMD, type:

ping google.com


Press Enter

Output you will see

Reply from google.com

Time = … ms

Shows if network is working.

2️⃣ IPCONFIG
Purpose: View IP address information.
Steps

Type:

ipconfig


Press Enter

To view full details:
ipconfig /all

Output you will see

IPv4 address

Subnet mask

Default gateway

DNS servers

3️⃣ TRACERT
Purpose: Shows the route/path packets take to reach a site.
Steps

Type:

tracert www.google.com


Press Enter

Output

List of routers/hops

Stops if a router is down

4️⃣ NETSTAT
Purpose: View active network connections and ports.
Steps

Type:

netstat


For detailed version:

netstat -f

Output

Active TCP connections

Local & foreign addresses

Connection state

5️⃣ NSLOOKUP
Purpose: Get IP from domain name or domain name from IP.
Steps

To find IP of a website:

nslookup www.example.com


To reverse lookup (IP → name):

nslookup 8.8.8.8

6️⃣ ROUTE
Purpose: View and edit routing table.
Steps

To view routing table:

route print


To add a route (example):

route add 192.168.1.0 mask 255.255.255.0 192.168.1.1


To delete a route:

route delete 192.168.1.0

7️⃣ ARP
Purpose: Shows IP → MAC address mappings.
Steps

Type:

arp -a


Press Enter

Output

IP address

MAC address

Type (dynamic/static)
