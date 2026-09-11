<div align="center">

# 🔐 Cybersecurity Lab Environment Setup 💻
**A controlled virtual cybersecurity laboratory built for learning and authorized penetration testing and ethical hacking practice.**


<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ver-Virtualbox%20v7.2-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Linux-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Virtualization-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Kali%20Linux-404040?style=flat-square&labelColor=C00000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Praveen Basava-C00000?style=flat-square" />

  **VirtualBox • Kali Linux • Virtual Networking • Linux Networking**
</p>
</div>

---

## 📌 Project Overview

This project involves setting up a virtual cybersecurity and penetration-testing laboratory using VirtualBox and Kali Linux. The lab provides a secure, isolated environment for practicing network scanning, reconnaissance, vulnerability assessment, and penetration testing. It uses a private virtual network and can be expanded with additional virtual machines for authorized security testing.

---

## 🎯 Objectives

*The key objectives of this project are to :*
- Set up and configure VirtualBox.
- Install and configure Kali Linux as a virtual machine.
- Create a private NAT Network for the lab.
- Configure and verify Kali Linux network connectivity.
- Assign a consistent IP address to the Kali VM.
- Verify internet and DNS connectivity.
- Create a clean VM snapshot for recovery.
- Document the complete laboratory setup.
- Prepare the environment for future cybersecurity testing.

---

## 🖥️ Purpose of the Lab
**The lab is intended to provide a controlled virtual environment for cybersecurity training, experimentation, and authorized penetration testing.**

*It supports activities such as :*
- Network reconnaissance and scanning
- Vulnerability assessment
- Packet and traffic analysis
- Web application security testing
- Penetration-testing practice
- Cybersecurity tool evaluation

---

## ⚙️ Lab Architecture
**The lab runs on Ubuntu Linux as the host operating system, with VirtualBox providing the virtualization platform. Kali Linux is deployed as a virtual machine and connected to a dedicated NAT Network for isolated and controlled cybersecurity testing.**
<img width="1920" height="1079" alt="1-Screenshot-environment" src="https://github.com/praveenbasava99/NETWORKWALKS-B083-W1-PM1-CYBERSECURITY-LAB-SETUP-/blob/main/1-Screenshot-environment.png?raw=true" />
*Additional target machines can be added to the same **virtual network** in future projects, enabling more advanced cybersecurity testing and lab exercises.*

## 🛠️ Lab Configuration

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 🖥️ Host OS       | Ubuntu 26.04 |
| 💾 Host RAM      | 6 GB |
| ⚡ Processor      | Intel(R) Core(TM) |
| 📦 Hypervisor     | VirtualBox 7.2.16 |
| 🐉 Security OS   | Kali Linux 2026.2 |
| 💾 Kali RAM       | 2048 MB |
| 🌐 Virtual Network | NAT Network |
| 📡 Network Range  | 10.0.0.0/24 |
| 🐉 Kali IP        | 10.0.0.3/24 |
| 🚪 Default Gateway | 10.0.0.1 |
| 🌍 DNS Server     | 8.8.8.8 |
| 🔮 Future VM Range | 10.0.0.4–10.0.0.99 |

---

## 🛡️ Lab Setup Procedure
### Step 1: Install VirtualBox

Oracle VirtualBox 
<img width="147" height="147" alt="image" src="https://github.com/user-attachments/assets/c825631f-1e55-422b-973e-9aca73338105" />

---

## Step 2: Configure the NAT Network

**A dedicated NAT Network was created in VirtualBox to provide network connectivity between the virtual machines while maintaining outbound internet access.**

**Network Configuration :**

| *Parameter*	| *Configuration* |
|---|---|
| Network Name |	NatNetwork |
| IPv4 Prefix |	10.0.0.0/24 |
| DHCP | Enabled |
| IPv6 |	Disabled |

<img width="1920" height="1079" alt="2-Screenshot-network-setting" src="https://github.com/praveenbasava99/NETWORKWALKS-B083-W1-PM1-CYBERSECURITY-LAB-SETUP-/blob/5916e9911d3d95da72d72ed3981569991d2632a3/2-Screenshot-network-settings.png"
/>

*🌐 The NAT Network provides a shared virtual network in which the lab machines can communicate with each other. This creates the foundation for deploying and testing attacker and target systems in an isolated cybersecurity lab environment.*

---

## Step 3: Import Kali Linux
**The Kali Linux virtual machine was downloaded from the official Kali Linux website and imported into VirtualBox.**

*The VM network adapter was configured as follows:*

| Adapter 1 | 
|---|
| Attached to: NAT Network |
| Network:     NatNetwork |
| Adapter Type: Intel PRO/1000 MT Desktop |

The VM was allocated: 
RAM: 2048 MB

<img width="1920" height="1079" alt="3-Screenshot-kali-linux" src="https://github.com/praveenbasava99/NETWORKWALKS-B083-W1-PM1-CYBERSECURITY-LAB-SETUP-/blob/main/3-network%20adapter.png?raw=true" />

*A shared folder was enabled to allow convenient file exchange between the host system and the Kali Linux VM.*

---

### Step 4: Configure the Kali Linux Network

**The Kali Linux network interface was configured with a static IPv4 address for consistent connectivity and easier identification within the lab.**

| Configuration : |
|---|
| IP Address:    10.0.0.3 |
| Netmask:   24 |
| Gateway:       10.0.0.1 |
| DNS:           8.8.8.8 |

<img width="1920" height="1080" alt="Kali Linux Network Settings" src="https://github.com/praveenbasava99/NETWORKWALKS-B083-W1-PM1-CYBERSECURITY-LAB-SETUP-/blob/main/5.png?raw=true" />

*Using a consistent IP address simplifies network configuration and makes the Kali Linux machine easier to reference during future lab exercises.*

---

### Step 5: Create a Clean VM Snapshot

After completing the initial Kali Linux configuration, a VirtualBox snapshot was created to preserve the current system state.

**Snapshot Name:** my fresh kali linux after installation
<img src="https://github.com/praveenbasava99/NETWORKWALKS-B083-W1-PM1-CYBERSECURITY-LAB-SETUP-/blob/main/6.png?raw=true" />

This snapshot serves as the baseline state of the lab. It allows the VM to be quickly restored if future experiments modify or disrupt the system configuration.

---

## 🔍 Lab Verification

| Check                 | Command                     | Expected Result       |
| --------------------- | --------------------------- | --------------------- |
| 📌 IP Check           | `ip a`                      | Correct Kali IP shown |
| 🚪 Gateway Check      | `ping 10.0.0.3`             | Replies received      |
| 📡 Connectivity Check | `ping 8.8.8.8`              | Internet reachable    |
| 🗂️ DNS Check         | `nslookup networkwalks.com` | Domain resolved       |
| 🔄 Snapshot Check     | Restore → `ip a`            | Baseline restored     |

**Result:** ✅ All verification checks passed successfully.

<img width="1920" height="1080" alt="Kali Linux Network Settings" src="https://github.com/praveenbasava99/NETWORKWALKS-B083-W1-PM1-CYBERSECURITY-LAB-SETUP-/blob/main/VirtualBox_kali-linux-2026.2-virtualbox-amd64_11_09_2026_23_10_01.png?raw=true" />

### Example Results

| IP Address | Gateway | Dns |
| --- | --- | --- |
| 10.0.0.3/24 |10.0.0.1 | 8.8.8.8 |

---

### ⚠️ Problems Encountered


### Problem 1. Internet Connectivity After Static IP Configuration

**After manually configuring the IPv4 settings, Internet connectivity may stop working due to NetworkManager or gateway configuration.**

### Problem 2: DNS Resolution Failure

**Problem: After configuring the network, the Kali Linux VM could reach IP addresses, but domain names were not resolving. This indicated an issue with the DNS configuration.**

---

## 🧠  What I Learned

This project provided hands-on experience in building a basic cybersecurity lab using VirtualBox and Kali Linux.

### 🌐 Networking

Understood NAT and NAT Network configurations and how they enable communication between virtual machines.

### 💻 Kali Linux

Gained practical experience configuring IP addresses, gateways, subnet masks, and DNS.

### 🔄 Recovery

Learned how VM snapshots can be used to preserve a stable configuration and quickly recover from configuration issues.

### 🛠️ Troubleshooting

Practiced identifying and resolving common networking and DNS-related problems.

### 📝 Documentation

Improved my ability to document technical configurations, testing procedures, issues, and solutions in a structured manner.

**Overall:** This project strengthened my understanding of **virtualization, networking, Linux administration, and cybersecurity lab practices**.

---

## 🔗 Tools & Resources

- **7-Zip**
https://7-zip.org/download.html
- **VirtualBox:** https://virtualbox.org/wiki/Downloads
- **Kali Linux:** https://kali.org/get-kali

---

## 👤 Author

**Praveen Basava**
Cybersecurity Intern | Networkwalks Academy — Batch B083

**LinkedIn:** [www.linkedin.com/in/praveen-basava)

---

## 📌 Project Information

| Details        | Information                          |
| -------------- | ------------------------------------ |
| **Program**    | Cybersecurity at Networkwalks        |
| **Week**       | 01                                   |
| **Project**    | Cybersecurity & Pentesting Lab Setup |

---


