# <h1 align="center">🔓🔑Cybersecurity Environment Lab Setup</h1>

Developing a practical cybersecurity lab to explore penetration testing, ethical hacking, and real-world security techniques in a controlled environment.

---
## 📌 Project Overview

This project focuses on creating a controlled cybersecurity environment using **VirtualBox and Kali Linux**.

The lab helped me understand virtual machine networking, IP configuration, connectivity testing, and VM snapshots. It can also be expanded later by adding additional virtual machines for authorized security testing.

---

## 🎯 Objectives

- Configure VirtualBox.
- Install and configure Kali Linux.
- Create a dedicated NAT Network.
- Configure Kali Linux networking.
- Assign a consistent IPv4 address.
- Configure gateway and DNS.
- Test network and internet connectivity.
- Verify DNS resolution.
- Create a clean VM snapshot.
- Document the complete setup.
- Prepare the lab for future cybersecurity projects.

---

## 🛡️ Purpose of the Lab

This laboratory provides a controlled environment for practicing cybersecurity concepts safely.

It can be used for:

- Network reconnaissance
- Port scanning
- Vulnerability assessment
- Packet analysis
- Web security testing
- Security-tool practice
- Penetration-testing exercises

> ⚠️ **Ethical Use:** Only test systems that you own or have explicit permission to test.

---

## 🏗️ Lab Architecture


                Host Computer
                     │
                     ▼
                 VirtualBox
                     │
                     ▼
                NAT Network
                 10.0.0.0/24
                     │
                     ▼
                 Kali Linux
                  10.0.0.2


## ⚙️ Lab Configuration
Component	Configuration
Host OS	Windows 10
Virtualization	VirtualBox
Security OS	Kali Linux
Kali RAM	2048 MB
Virtual Network	NAT Network
Network Address	10.0.0.0/24
Kali IP	10.0.0.2
Gateway	10.0.0.1
DNS	8.8.8.8
🧰 Tools Used
VirtualBox
Kali Linux
7-Zip
Nmap
Linux networking utilities
GitHub

### 🛠️ Lab Setup Process Step 1 — Install 7-Zip

7-Zip was used to extract the Kali Linux virtual-machine package before importing it into VirtualBox.

📷 Screenshot: Add your own 7-Zip screenshot here.

### Step 2 — Install VirtualBox

VirtualBox was installed as the virtualization platform for creating and managing the cybersecurity lab.

📷 Screenshot: Add your own VirtualBox screenshot here.

### Step 3 — Create the NAT Network

A dedicated NAT Network was created for the lab.

Network Name: NatNetwork
IPv4 Prefix:  10.0.0.0/24
DHCP:         Enabled
IPv6:         Disabled

This allows multiple virtual machines to communicate through the same virtual network while maintaining external connectivity.

📷 Screenshot: Add your NAT Network screenshot here.

### Step 4 — Import Kali Linux

Kali Linux was imported into VirtualBox and connected to the NAT Network.

Adapter:       Adapter 1
Network Mode:  NAT Network
Network Name:  NatNetwork
Adapter Type:  Intel PRO/1000 MT Desktop
RAM:           2048 MB

A shared folder was also configured for convenient file transfer between the host and Kali VM.

📷 Screenshot: Add your Kali Linux screenshot here.

### 🌐 Step 5 — Configure Kali Linux Network

The Kali network configuration was checked and configured with a consistent IPv4 address.

IP Address:    10.0.0.2
Subnet Mask:   255.255.255.0
Gateway:       10.0.0.1
DNS:           8.8.8.8

A consistent IP makes the Kali machine easier to identify during future lab exercises.

📷 Screenshot: Add your network configuration screenshot here.

### 💾 Step 6 — Create a Clean VM Snapshot

After completing the basic configuration, a VirtualBox snapshot was created.

Snapshot Name:
Clean Kali - Network Setup

This provides a recovery point that can be used if future experiments change the VM configuration.

📷 Screenshot: Add your snapshot screenshot here.

🧪 Lab Verification

The environment was tested after configuration.

Test	Check	Expected Result
IP Address	ip a	Correct IP displayed
Gateway	ping 10.0.0.1	Successful replies
Internet	ping 8.8.8.8	Successful replies
DNS	nslookup networkwalks.com	Domain resolves
Nmap	nmap --version	Version displayed
Snapshot	VirtualBox	Snapshot available
Example Result
IP Address: 10.0.0.2/24
Gateway:    10.0.0.1
DNS:        8.8.8.8

📷 Screenshot: Add your verification screenshot here.

### 🐛 Problem Encountered & Solution
Internet Connectivity After Static IP Configuration

After manually configuring the IPv4 settings, internet connectivity did not work correctly.

I reviewed the Kali network configuration, restarted the network connection, and tested the connection again.

What I Learned

Static IP configuration requires the IP address, subnet mask, gateway, DNS, and virtual network to be configured correctly.

Network interface names may differ between Linux systems, so they should always be checked before applying network commands.

### 💡 What I Learned
1. NAT Network

I learned how a NAT Network allows multiple virtual machines to communicate through a shared virtual network while providing external connectivity.

2. VM Networking

I learned how VirtualBox network adapters connect virtual machines to different network types.

3. Static IP Configuration

I gained practical experience with IPv4 addresses, subnet masks, gateways, and DNS configuration in Kali Linux.

4. VM Snapshots

Snapshots provide a reliable recovery point before performing experimental changes.

5. Documentation

I learned the importance of recording configurations, screenshots, testing results, and troubleshooting steps during a cybersecurity project.

### 🔐 Security & Ethical Use

This project is intended strictly for educational and authorized cybersecurity practice.

All testing should be performed only on systems that I own or have explicit permission to test.

🔗 Tools & Resources
7-Zip
VirtualBox
Kali Linux

### 👤 Author

Your Name

Cybersecurity Learner | Networking | Ethical Hacking


LinkedIn: Add your LinkedIn profile


### 📋 Project Information
Project	Cybersecurity Lab Environment
Focus	Virtualization & Networking
Platform	VirtualBox
Security OS	Kali Linux
Network	10.0.0.0/24
Lab IP	10.0.0.2
Status	Completed


### 🚀 Future Improvements
Add vulnerable target machines
Practice web application security
Perform network scanning exercises
Practice packet analysis
Add vulnerability-assessment labs
Add network monitoring
Expand the virtual lab environment

### ⭐ Final Note
This project is the foundation of my personal cybersecurity laboratory. I plan to continue expanding it with additional virtual machines and hands-on cybersecurity exercises.

