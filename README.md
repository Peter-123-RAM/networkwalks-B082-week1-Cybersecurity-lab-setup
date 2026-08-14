Networkwalks B082 — Week 1 Cybersecurity Lab Setup

"Cybersecurity" (https://img.shields.io/badge/Focus-Cybersecurity-red)
"Platform" (https://img.shields.io/badge/Platform-Kali%20Linux-blue)
"Virtualization" (https://img.shields.io/badge/Virtualization-VirtualBox-orange)
"Network" (https://img.shields.io/badge/Network-10.0.0.0%2F24-green)

Overview

This repository documents my Week 1 Cybersecurity and Ethical Hacking Lab Setup completed as part of the Networkwalks B082 training program.

The laboratory was built using Oracle VirtualBox with Kali Linux as the primary cybersecurity environment. A dedicated NAT Network was configured to provide controlled communication between virtual machines for authorized cybersecurity training and practical exercises.

---

Objectives

The lab setup focused on:

- Installing the required laboratory software.
- Deploying Oracle VirtualBox as the virtualization platform.
- Creating a dedicated VirtualBox NAT Network.
- Importing and configuring Kali Linux.
- Configuring static IPv4 networking within the virtual laboratory.
- Verifying the network configuration.
- Establishing a controlled environment for future cybersecurity and ethical hacking exercises.

---

Lab Environment

Component| Configuration
Host Platform| Windows
Hypervisor| Oracle VirtualBox
Security Operating System| Kali Linux
Network Type| NAT Network
IPv4 Network| "10.0.0.0/24"
Kali Linux IP| "10.0.0.2/24"
Gateway| "10.0.0.1"
DNS Server| "10.0.0.1"
Archive Utility| 7-Zip
Connectivity Test| "ping"

---

Phase 1 — Core Laboratory Setup

1. 7-Zip Installation

7-Zip was installed to support the extraction of compressed virtual machine images and other laboratory resources required during the setup process.

---

2. Oracle VirtualBox Installation

Oracle VirtualBox was installed and configured as the hypervisor for the cybersecurity laboratory.

VirtualBox provides the virtualization layer required to run and manage isolated operating systems for cybersecurity practice.

---

3. NAT Network Configuration

A dedicated NAT Network was configured in VirtualBox to provide a private network environment for communication between virtual machines.

Network Configuration

Network Name: NATNetwork
IPv4 Network: 10.0.0.0/24
Gateway: 10.0.0.1

The "/24" prefix provides a private IPv4 network suitable for the laboratory environment.

---

4. Kali Linux Deployment

Kali Linux was imported into Oracle VirtualBox and configured as the primary cybersecurity workstation.

Kali Linux provides a specialized environment containing tools used for security assessment, network analysis, penetration testing, vulnerability assessment, and ethical hacking.

Virtual Machine Configuration

The configured Kali Linux virtual machine was allocated:

Memory: 4096 MB
Processors: 2
Virtual Disk: 50 GB

---

5. Kali Linux IPv4 Configuration

Kali Linux was configured with a manual IPv4 address within the laboratory network.

Network Configuration

IPv4 Address: 10.0.0.2
Netmask: /24
Gateway: 10.0.0.1
DNS Server: 10.0.0.1

This configuration places the Kali Linux virtual machine within the "10.0.0.0/24" laboratory network.

Configuration Evidence

"Kali Linux IPv4 Configuration" (screenshots/03-kali-network-configuration.png)

---

6. Kali Linux Virtual Machine

The Kali Linux virtual machine was successfully launched through Oracle VirtualBox.

"Kali Linux Virtual Machine" (screenshots/01-kali-virtualbox.png)

The virtual machine provides the primary environment for the cybersecurity exercises in the laboratory.

---

7. Kali Linux Boot Environment

The Kali Linux boot environment was successfully initialized within the VirtualBox virtual machine.

"Kali Linux Boot Environment" (screenshots/02-kali-boot.png)

---

Network Architecture

The laboratory network is structured around a private VirtualBox NAT Network:

                    Host Computer
                         │
                    Oracle VirtualBox
                         │
                    NAT Network
                    10.0.0.0/24
                         │
                  ┌──────┴──────┐
                  │             │
             Kali Linux     Other VMs
             10.0.0.2       10.0.0.x
             /24
                  │
             Gateway
             10.0.0.1

This architecture provides a controlled environment for authorized cybersecurity training.

---

Network Verification

Network connectivity can be verified using the "ping" utility.

Example:

ping 10.0.0.1

The purpose of the connectivity test is to confirm communication between the Kali Linux virtual machine and the configured network gateway or other authorized laboratory systems.

---

Security Considerations

This laboratory is intended strictly for authorized cybersecurity training, education, and ethical hacking practice.

Virtual machines provide a controlled environment for experimenting with security tools and networking techniques without intentionally targeting unauthorized systems.

All security testing should be performed only against systems for which appropriate authorization has been obtained.

---

Key Learning Outcomes

Through this laboratory setup, I gained practical experience in:

- Virtualization using Oracle VirtualBox.
- Deploying Kali Linux in a virtual environment.
- Creating and configuring a NAT Network.
- Working with private IPv4 addressing.
- Understanding CIDR notation.
- Configuring static IPv4 settings in Linux.
- Configuring gateways and DNS.
- Understanding virtual machine networking.
- Establishing a controlled cybersecurity laboratory.
- Preparing an environment for future ethical hacking and security testing exercises.

---

Conclusion

The Networkwalks B082 Week 1 laboratory established the foundation for practical cybersecurity and ethical hacking training.

The completed setup combines Kali Linux, Oracle VirtualBox, and a dedicated "10.0.0.0/24" virtual network to provide a controlled environment for subsequent security exercises.

This practical strengthened my understanding of virtualization, Linux networking, IP addressing, and secure laboratory design while preparing the environment for future cybersecurity challenges.

---

Author

Adongo Peter Oduor

Networkwalks B082
Cybersecurity & Ethical Hacking

---

Repository Structure

networkwalks-B082-week1-Cybersecurity-lab-setup/
│
├── README.md
│
└── screenshots/
    ├── 01-kali-virtualbox.png
    ├── 02-kali-boot.png
    └── 03-kali-network-configuration.png

---

Training Program

Networkwalks B082 — Week 1

Focus: Cybersecurity & Ethical Hacking Lab Setup
