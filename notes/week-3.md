# Week 3: Linux and Networking
## What is Networking

Networking is the practice of connecting computers so they can share information. You can think of it as a huge highway system where data travels from one place to another. When devices are connected, they can share files, use shared printers, access internet resources, communicate through email or chat, and store information in centralized locations instead of keeping everything separately.

## Key Networking Terms

- A protocol is simply a set of rules that computers follow to communicate. Examples include HTTP for websites, TCP or IP for reliable communication, and FTP for transferring files.
- Bandwidth refers to how much data can be transferred at once. A higher bandwidth is like having a wider highway with more lanes so traffic can move faster.
- A router directs traffic between networks. It plays a similar role to a traffic officer guiding vehicles from one road to another.
- A firewall acts as a security barrier. It decides which traffic is allowed and which traffic should be blocked in order to protect the network from threats.

## Common Network Types

- A local area network, or LAN, covers a small area such as a home or office. It is fast, private, and easy to secure. Your home WiFi is a typical example.
- A wide area network, or WAN, spans large geographic areas such as countries or continents. The internet itself is the most common example because it connects millions of smaller networks together.
- A virtual private network, or VPN, creates a secure path over the internet. Even though your data travels through public infrastructure, it is encrypted so that it behaves like a private tunnel.

## The OSI Model

- The OSI model breaks networking into seven layers, similar to how a post office handles mail.
- The application layer is where users interact with services such as websites or email.
- The presentation layer prepares data so it can be transmitted, which includes tasks like encryption and formatting.
- The session layer manages the communication between two devices and keeps the connection active.
- The transport layer ensures data is delivered properly through TCP or UDP and uses port numbers to direct communication.
- The network layer handles IP addressing and decides how data moves from one network to another.
- The data link layer is concerned with physical identification using MAC addresses on switches.
- The physical layer includes the actual cables, WiFi signals, and electrical transmissions that move bits across the network.

## TCP and UDP

- TCP focuses on accuracy. It checks that all data arrives correctly, making it reliable for web browsing or email. This reliability makes it slower.
- UDP focuses on speed. It sends data quickly without checking if everything arrived. Because of this, it is often used for online gaming, streaming, or video calls where speed is more important than perfection.

## IP Addresses

- Every device on a network needs an IP address, which acts like its home address.
- IPv4 uses four numbers and is still the most commonly used type, but it is running out of available addresses.
- IPv6 uses a much larger format that includes letters and allows for an almost unlimited number of devices.

There are also special IP addresses worth knowing. The address 127.0.0.1 refers to your own computer and is known as localhost. The address 0.0.0.0 represents any address, while 255.255.255.255 is used for broadcast messages that go to every device in a network.

## Public and Private IP Addresses

- A public IP address is visible on the internet and can be accessed from anywhere in the world, similar to a home’s street address. Servers that need to be reachable from the outside world use public IPs.
- A private IP address only works inside a private network and cannot be reached directly from the internet. It is similar to an apartment number inside a building. Private networks often reuse the same ranges of IPs. These ranges include the 10.x.x.x network, the 172.16.x.x to 172.31.x.x range, and the 192.168.x.x network.

## AWS Networking and VPC

- A Virtual Private Cloud, or VPC, is your own private network inside AWS. It functions like a personal data center in the cloud. Inside a VPC you can create subnets, which divide the network into smaller sections. A public subnet contains resources that need internet access, while a private subnet is designed for things like databases that should not be exposed.
- An internet gateway connects the VPC to the internet, and a NAT gateway allows resources in private subnets to access the internet without being directly exposed. A typical setup includes a VPC with one public subnet for web servers and one private subnet for internal databases.

## Network Troubleshooting Commands

Several commands help diagnose network issues. The ping command checks whether a device is reachable. The traceroute command shows the path data takes to reach a destination. The nslookup command checks how DNS resolves a domain name. Other tools like ip addr show network interfaces, while netstat and ss display active connections and listening ports.

## Systematic Troubleshooting

- A clear process helps solve networking problems.
- First, define the problem and identify when it started and what changed recently.
- Next, check the physical layer by ensuring cables are plugged in, WiFi is enabled, and devices are powered on.
- Test the local network by pinging your own computer and your router.
- After that, test internet connectivity using public IP addresses like 8.8.8.8.
- If the internet works using an IP but not a website name, the issue is likely with DNS.

## Week 3 Key Takeaways

- Networking allows computers to communicate and share information efficiently.
- IP addresses act like home addresses for digital devices.
- TCP prioritizes reliable delivery while UDP prioritizes speed.
- Private IPs are meant for internal communication and public IPs allow internet access.
- A VPC in AWS provides a secure and customizable cloud network.
- Public subnets allow access to the internet while private subnets do not.
- Understanding the seven OSI layers provides a structured view of how data travels.
- Troubleshooting always begins with checking the simplest, physical components.

## Personal Note

Networking felt complicated at first because it introduced so many new concepts ranging from protocols to IP addressing. Once I started comparing it to familiar systems like postal delivery it became much easier to understand. Realizing that data follows routes, has addresses, and is delivered using different methods made everything far more logical. Learning to troubleshoot issues by checking one layer at a time completely changed the way I approach problems and made networking feel much more manageable.