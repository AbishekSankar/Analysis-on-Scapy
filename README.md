# About this project - Analysis On Scapy

## Abstract

&emsp;&emsp; Scapy is a Python-based packet manipulation environment that is free and open-source. Many people consider Scapy to be one of the most significant tools for dealing with packages. It opens up a lot of opportunities and is a terrific way to broaden your network expertise. This report will include a brief overview of scapy and its features, as well as examples, explanations, and thorough step-by-step documentation for the scapy functions. It will also cover learning and using the tools in real-world scenarios.

## What is Scapy?

&emsp;&emsp; Scapy is a strong packet modification application that can be used interactively. It can spoof or decode packets from a variety of protocols, send them over the network, collect them, match requests and responses, and much more. Scanning, tracerouting, probing, unit testing, assaults, and network discovery are all simple chores for it (it can replace hping, 85 percent of nmap, arpspoof, arp-sk, arping, tcpdump, tethereal, p0f, etc.). It also excels at a variety of additional jobs that most other programmes can't, such as sending incorrect frames, injecting your own 802.11 packets, combining techniques (VLAN hopping+ARP cache poisoning, VOIP decoding on a WEP encrypted channel, and so on), and so on.

## What is the purpose of Scapy?

- Scapy, when used in the field of computer security, allows us to conduct scans and/or network assaults.
- Scapy's key advantage is that, unlike other tools, it allows us to modify network packages at a low level, allowing us to use existing network protocols and parameterize them according to our requirements and, if we opt to use your Python libraries, we will be able to create our own tools, and in this manner, we will be able to create other higher-level advancements and combine them all according to our requirements.

## Features of Scapy

Scapy provides us with a lot more functionalities than any other tool or module. Here are some of its features:

- Can craft any packet and encode it.
- Sniffing network packets.
- Sending valid/invalid frames.
- Injecting your own 802.11 frames.
- Editing network packets on the fly.
- Scanning the network. and Tracerouting and probing.
- Attacking networks. \& Network discovery.

## Installation of Scapy

- I was able to instal dependencies for Scapy's operation after reading and understanding the manual.For cloning Scapy's develoient repository to my local PC, I'll need Git.
  ![i1](/screenshots/i1.png)

- Finished the installation Some Python modules and apt packages that are required for Scapy to function.
  ![i2](/screenshots/i2.png)
  ![i3](/screenshots/i3.png)

- Cloning Scapy's develoient repository to my own system, as per the published docs.
  ![i4](/screenshots/i4.png)

- Scapy was successfully installed on my local workstation after running the setup.py file in the cloned folder
  ![i5](/screenshots/i5.png)

- Executing Scapy
  ![i6](/screenshots/i6.png)

## Implementation

### Packet Sniffing

- Open scapy as sudo user
  ![ps1](/screenshots/ps1.png)
- Sniffing packets and displaying basic information such as the packet layers. The sniff() function is used to sniff packets. The count parameter specifies the number of packets to capture. summary() displays the packet's. basic information, such as its layers. The network layer is ether, the Internet layer is IP, the transport layer is UDP/TCP, and the application layer is DNS.
  ![ps1](/screenshots/ps2.png)
- While sniffing the packets, run the summary() function.
  ![ps3](/screenshots/ps3.png)
- Sniffing packets from my "wlp2s0" wireless network interface.
  ![ps4](/screenshots/ps4.png)
- The show() function displays precise information about the packet that was captured.
  ![ps5](/screenshots/ps5.png)
  ![ps6](/screenshots/ps6.png)

## Reading and analysis from pcap files

- To generate a pcap file, open Wireshark as a sudo user.
  ![pc1](/screenshots/pc1.png)
- Generating pcap file using wireshark.
  ![pc1](/screenshots/pc2.png)
- Saving pcap file in the local directory.
  ![pc1](/screenshots/pc3.png)
- Opening scapy, reading the pcap file, and displaying the packet's summary and length. Assigning a packet to a variable and viewing its contents, including a hexdump representation and basic information.
  ![pc1](/screenshots/pc4.png)
- pkt.show() will display the pkt's complete information.
  ![pc1](/screenshots/pc5.png)

## Packet Manipulation

- The fundamentals of making a packets.
  ![pc1](/screenshots/pm1.png)
- Now I'll create a packet and transmit it to my loop-back address.
  ![pc1](/screenshots/pm2.png)
- The traffic of my loop-back IP was captured using Wireshark.
  ![pc1](/screenshots/pm3.png)
- Creating and sending a packet to my loop-back address with an ICMP layer and raw data.
  ![pc1](/screenshots/pm4.png)
- The traffic of my loop-back IP was captured using Wireshark.
  ![pc1](/screenshots/pm5.png)
- Sending and receiving packets with the ICMP layer and raw data to and from my wifi network interface "wlp2s0".
  ![pc1](/screenshots/pm6.png)
- The traffic of my wifi network interface "wlp2s0" was captured using Wireshark.
  ![pc1](/screenshots/pm7.png)
- Sending and receiving a single packet to and from my gateway address.
  ![pc1](/screenshots/pm8.png)
- Using a custom DNS query, sending and receiving packets from Google DNS server "8.8.8.8."
  ![pc1](/screenshots/pm9.png)
  ![pc1](/screenshots/pm10.png)
- Sending and receiving packets from www.google.com using random TCP source ports, then plotting the data.
  ![pc1](/screenshots/pm11.png)
  ![pc1](/screenshots/pm12.png)

## What way the project could have been made better?

- While learning about packet sniffing using scapy I came across the tool, SolarWinds Network Performance Monitor (NPM). It is a multi-layered tool that provides a comprehensive view of your network, so we can quickly detect, diagnose, and resolve network performance issues and avoid downtime.
- SolarWinds Network Packet Sniffer has a WiFi packet capture tool. It can differentiate normal traffic from abnormal traffic and provides detailed data and transaction volume according to the application. These insights will help us with spotting the problem and avoid the network.
- This is a crucial function that scapy lacks; it just sniffs packets and displays packet information, but it lacks the insights that the SolarWinds Network Packet Sniffer provides. As a result, it would be preferable if these insights features were added in the future.
- Scapy should be faster and more efficient at analyzing packets from pcap files, although its competitor dpkt reads and analyses pcap files more efficiently. As a result, scapy needs to improve in this area.
- The newest version of python is 3.9, scapy hasn't updated its codebase to the newest python version which much faster than the current version.

## What more can be done in this project?

- GUI Support:<br/>
  &emsp;&emsp; Scapy doesn't have a graphical user interface. While most of its competitors, such as Wireshark and others, have GUI and web-based applications, scapy only has a command-line interpreter, which is a disadvantage for newcomers learning ethical hacking or other network-related topics. Analyzing and deriving information from packets and visually displaying it is far preferable to viewing it from the command line.

- Documentation:
  - Scapy documentation is available on its website for installation and learning its functionalities, however, the problem is that it lacks good documentation for scapy development. If a beginner wants to contribute to scapy, there is no clear path for learning how to construct modules in scapy. In the development of Scapy, everything is done by hand, which is extremely difficult for beginners.
  - Scapy is incapable of handling a high number of packets at the same time. Scapy should have more efficient and stable features so that it can manage a huge number of packets at once.
  - Certain complex protocols are partially supported by scapy.

## Reference and Research

- Official Site of Scapy : <https://scapy.net/>
- Scapy Documentation : <https://scapy.readthedocs.io/en/latest/>
- Github Source Code of Scapy : <https://github.com/secdev/scapy>
- A Unofficial Guide to Scapy : <https://theitgeekchronicles.files.wordpress.com/2012/05/scapyguide1.pdf>
