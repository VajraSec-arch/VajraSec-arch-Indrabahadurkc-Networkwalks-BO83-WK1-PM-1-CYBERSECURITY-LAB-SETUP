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


<img width="2786" height="1614" alt="Screenshot 2026-09-05 091919" src="https://github.com/user-attachments/assets/dd9bb93e-4c1e-4b5b-82d7-8997f2ec8380" />


### Step 2 — Install VirtualBox

VirtualBox was installed as the virtualization platform for creating and managing the cybersecurity lab.


<img width="2848" height="1632" alt="Screenshot 2026-09-03 063953" src="https://github.com/user-attachments/assets/4a6ed265-5b7b-4886-96ad-a02251fbaeb9" />



### Step 3 — Create the NAT Network

A dedicated NAT Network was created for the lab.

Network Name: NatNetwork
IPv4 Prefix:  10.0.0.0/24
DHCP:         Enabled
IPv6:         Disabled

This allows multiple virtual machines to communicate through the same virtual network while maintaining external connectivity.

<img width="2872" height="1808" alt="Screenshot 2026-09-03 071151" src="https://github.com/user-attachments/assets/264a694f-99f2-4fc9-b31b-a1416675e35e" />


### Step 4 — Import Kali Linux

Kali Linux was imported into VirtualBox and connected to the NAT Network.

Adapter:       Adapter 1
Network Mode:  NAT Network
Network Name:  NatNetwork
Adapter Type:  Intel PRO/1000 MT Desktop
RAM:           2048 MB

A shared folder was also configured for convenient file transfer between the host and Kali VM.
<img width="2858" height="1720" alt="Screenshot 2026-09-05 082823" src="https://github.com/user-attachments/assets/d0164e58-0e03-4919-8483-3ca339a8542a" />


### 🌐 Step 5 — Configure Kali Linux Network

The Kali network configuration was checked and configured with a consistent IPv4 address.

IP Address:    10.0.0.2
Subnet Mask:   255.255.255.0
Gateway:       10.0.0.1
DNS:           8.8.8.8

A consistent IP makes the Kali machine easier to identify during future lab exercises.
<img width="2812" height="1722" alt="Screenshot 2026-09-05 082911" src="https://github.com/user-attachments/assets/21108de2-082e-4ca5-a663-609b1e1c21aa" />



### 💾 Step 6 — Create a Clean VM Snapshot

After completing the basic configuration, a VirtualBox snapshot was created.

Snapshot Name:
Clean Kali - Network Setup

This provides a recovery point that can be used if future experiments change the VM configuration.
<img width="2880" height="1828" alt="Screenshot 2026-09-05 102402" src="https://github.com/user-attachments/assets/db0b88f1-efbf-468f-80a8-36e804ffcbdb" />



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

<img width="2870" height="1776" alt="Screenshot 2026-09-05 083007" src="https://github.com/user-attachments/assets/5c675b1c-06bf-412a-be62-0b3d878ec780" />


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
7-Zip:https://7-zip.org/download.html

VirtualBox:https://virtualbox.org/wiki/Downloads

Kali Linux:https://kali.org/get-kali

### 👤 Author
Waqas Karim
Cybersecurity Professional B083

LinkedIn:https://www.linkedin.com/in/waqaskarim/


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

