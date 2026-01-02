# CCNA-Static-Routing-Lab
A hands-on CCNA Static Routing lab implemented using Cisco Packet Tracer with 3 routers, 3 switches, and multiple networks.

📌 CCNA Static Routing – Cisco Packet Tracer Lab
📖 Overview

This project demonstrates Static Routing configuration using Cisco Packet Tracer as part of my CCNA learning journey.
The lab shows how routers communicate with multiple remote networks using manually configured static routes.

🧱 Lab Topology

Routers: 3

Switches: 3

End Devices: 6 Laptops

Routing Type: Static Routing

Each router is connected to a separate LAN, and routers are interconnected using WAN links.

🌐 IP Addressing Scheme

LAN Networks

Network	Subnet

LAN 1	192.168.1.0 /24
LAN 2	192.168.2.0 /24
LAN 3	192.168.3.0 /24
WAN Links
Link	Network
R1 ↔ R2	12.0.0.0
R2 ↔ R3	23.0.0.0
⚙️ Configuration Steps
1️⃣ Router Interface Configuration

Each router interface was configured using CLI with appropriate IP addresses.

Example:

interface fastEthernet0/0
ip address 12.0.0.1 255.0.0.0
no shutdown

2️⃣ Static Routing Configuration

🔹 Router 1 (R1)

ip route 23.0.0.0 255.0.0.0 12.0.0.2

ip route 192.168.2.0 255.255.255.0 12.0.0.2

ip route 192.168.3.0 255.255.255.0 12.0.0.2

🔹 Router 2 (R2)

ip route 192.168.3.0 255.255.255.0 23.0.0.3

ip route 192.168.1.0 255.255.255.0 12.0.0.1

🔹 Router 3 (R3)

ip route 192.168.1.0 255.255.255.0 23.0.0.2

ip route 12.0.0.0 255.0.0.0 23.0.0.2

ip route 192.168.2.0 255.255.255.0 23.0.0.2

🧪 Verification & Testing

Used ping command between laptops in different networks

Verified routing tables using:

show ip route


Successful ICMP replies confirmed correct static routing configuration

🎯 Key Learnings

Difference between directly connected and remote networks

How static routing works using next-hop IP

Importance of correct subnet mask and next-hop address

End-to-end connectivity testing using ping

🛠 Tools Used

Cisco Packet Tracer

CLI (IOS Commands)

🚀 Future Improvements

Implement Dynamic Routing (RIP / OSPF)

Add default route

Introduce routing failure testing

📎 Files Included

Cisco Packet Tracer (.pkt) file

Network topology diagram

Router configuration screenshots

Ping test results

👩‍💻 Author

Priyanshi Yadav
CCNA Aspirant | Networking Enthusiast


