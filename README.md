Networkwalks B082 — Week 1 Cybersecurity Lab Setup

Overview

This repository documents the setup and configuration of a virtualized cybersecurity and ethical hacking laboratory for Networkwalks B082 — Week 1.

The lab uses Oracle VirtualBox to create an isolated environment for cybersecurity practice. Kali Linux serves as the primary security testing platform, while additional virtual machines provide target environments for networking, security testing, and ethical hacking exercises.

---

Objectives

The objectives of this lab were to:

- Install the required virtualization and archive-management software.
- Configure Oracle VirtualBox for cybersecurity laboratory use.
- Create and configure a VirtualBox NAT Network.
- Import and configure Kali Linux as a virtual machine.
- Configure IP networking within the virtual laboratory.
- Create a stable restore point using VM snapshots.
- Configure additional virtual machines for future security exercises.
- Verify communication between virtual machines using network connectivity tests.

---

Lab Environment

Component| Configuration
Host Operating System| Windows
Hypervisor| Oracle VirtualBox
Primary Security VM| Kali Linux
Network Type| NAT Network
Virtual Network| "10.0.0.0/24"
Network Testing| "ping"
Archive Utility| 7-Zip

---

Phase 1 — Core Lab Setup

1. 7-Zip Installation

7-Zip was installed to provide support for extracting compressed virtual machine images and other laboratory resources.

---

2. Oracle VirtualBox Installation

Oracle VirtualBox was installed as the virtualization platform for creating, configuring, and managing the cybersecurity laboratory's virtual machines.

VirtualBox provides the isolated environment required to run multiple operating systems on the host computer.

---

3. VirtualBox NAT Network Configuration

A dedicated NAT Network was created in VirtualBox to provide network connectivity between the virtual machines.

Network Configuration

Network Name: NATNetwork
IPv4 Network: 10.0.0.0/24

The "10.0.0.0/24" network provides a private address space for communication between the laboratory machines while maintaining separation from the host's primary network environment.

---

4. Kali Linux Virtual Machine

Kali Linux was downloaded and imported into Oracle VirtualBox.

Kali Linux was configured as the primary cybersecurity workstation for the laboratory. It provides the tools and environment required for subsequent penetration testing, vulnerability assessment, network analysis, and ethical hacking exercises.

---

5. Kali Linux Network Configuration

The Kali Linux virtual machine was configured to operate on the laboratory NAT Network.

The configured network uses the "10.0.0.0/24" address range, allowing Kali Linux to communicate with other virtual machines connected to the same virtual network.

Network configuration was verified from within Kali Linux using standard Linux networking utilities.

---

6. Kali Linux Virtual Machine Snapshot

A snapshot of the configured Kali Linux virtual machine was created after completing the initial setup.

The snapshot provides a known-good restore point, allowing the virtual machine to be reverted to its configured state after future cybersecurity experiments or configuration changes.

---

Phase 2 — Additional Virtual Machines

Additional operating systems were prepared within VirtualBox to provide different environments for future cybersecurity and ethical hacking exercises.

The laboratory design includes:

- Windows 11
- Windows 10
- Windows 7
- Android 9.x

These systems provide different target environments for practical security testing and network-based exercises.

---

Network Connectivity Testing

Connectivity between the virtual machines was tested using the "ping" utility.

Example:

ping <target-ip-address>

The connectivity test was used to verify that machines connected to the configured NAT Network could communicate successfully.

---

Virtual Lab Architecture

                    Host Computer
                         │
                    VirtualBox
                         │
                  NAT Network
                  10.0.0.0/24
                         │
          ┌──────────────┼──────────────┐
          │              │              │
       Kali Linux      Windows       Android
       Security VM     Target VM      Target VM

The architecture provides a controlled virtual environment for conducting cybersecurity and ethical hacking exercises.

---

Security Considerations

The laboratory is designed for authorized cybersecurity training and educational purposes.

Using virtual machines provides an isolated environment in which security tools and techniques can be practiced without intentionally targeting unauthorized systems.

The environment should only be used against systems for which the user has explicit permission to perform security testing.

---

Challenges and Resolutions

During the laboratory setup, attention was required when configuring:

- Virtual machine networking.
- NAT Network parameters.
- IP addressing.
- Communication between virtual machines.
- Virtual machine resource allocation.
- Snapshot management.

These configuration requirements were addressed through VirtualBox settings, operating-system network configuration, and connectivity testing.

---

Key Learning Outcomes

By completing this laboratory, I gained practical experience in:

- Virtualization using Oracle VirtualBox.
- Building an isolated cybersecurity laboratory.
- Configuring virtual networks.
- Understanding private IP addressing and CIDR notation.
- Configuring Linux network interfaces.
- Deploying Kali Linux in a virtualized environment.
- Testing network connectivity between systems.
- Creating and managing virtual machine snapshots.
- Preparing controlled environments for cybersecurity and ethical hacking practice.

---

Conclusion

The Networkwalks B082 Week 1 laboratory established a functional virtual environment for cybersecurity and ethical hacking practice.

The combination of Kali Linux, VirtualBox, NAT networking, and additional target operating systems provides a controlled foundation for subsequent practical exercises involving network security, vulnerability assessment, penetration testing, and defensive security.

---

Author

Adongo Peter Oduor

Networkwalks B082
Cybersecurity & Ethical Hacking
