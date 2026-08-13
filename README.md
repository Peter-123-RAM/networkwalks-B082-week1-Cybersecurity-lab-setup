Networkwalks B082 — Week 1 Cybersecurity Lab Setup

📌 Overview

This project documents my Week 1 Cybersecurity and Ethical Hacking Lab Setup. The purpose of the lab was to create an isolated virtual environment for practicing cybersecurity, ethical hacking, networking, and penetration testing.

The lab was configured using Oracle VirtualBox with Kali Linux as the primary security testing machine and a NAT Network for communication between virtual machines.

---

🎯 Objectives

The main objectives of this lab were to:

- Install and configure the required virtualization software.
- Set up Oracle VirtualBox.
- Create and configure a NAT Network.
- Install and configure Kali Linux.
- Configure the IP address of the Kali Linux virtual machine.
- Take a snapshot of the configured Kali Linux VM.
- Prepare additional Windows/Android virtual machines for cybersecurity practice.
- Test connectivity between virtual machines using "ping".

---

🛠️ Tools and Technologies Used

- Oracle VirtualBox
- Kali Linux
- Windows virtual machines
- 7-Zip
- NAT Network
- Linux networking commands
- "ping"
- Virtual machine snapshots

---

🔹 PHASE 1: Initial Lab Setup

Step 1: Download and Install 7-Zip

I downloaded and installed 7-Zip to enable extraction of compressed virtual machine files and other required resources.

Status: ✅ Completed

Screenshot

«Add your screenshot here.»

"![7-Zip Installation](screenshots/7zip-installation.png)"

---

Step 2: Download and Install VirtualBox

I downloaded and installed Oracle VirtualBox on my computer.

VirtualBox was used as the virtualization platform for creating and managing the cybersecurity lab environment.

Status: ✅ Completed

Screenshot

«Add your screenshot here.»

"![VirtualBox Installation](screenshots/virtualbox-installation.png)"

---

Step 3: Configure the VirtualBox Network

I configured a NAT Network in VirtualBox to allow communication between the virtual machines in the cybersecurity lab.

Network Configuration

- Network Name: NATNetwork
- IPv4 Network: "10.0.0.0/24"
- DHCP: Configured according to the lab requirements

The NAT Network provides an isolated network environment where the virtual machines can communicate with each other.

Status: ✅ Completed

Screenshot

«Add your screenshot here.»

"![VirtualBox NAT Network](screenshots/nat-network.png)"

---

Step 4: Download and Import Kali Linux

I downloaded the Kali Linux virtual machine image and imported it into Oracle VirtualBox.

Kali Linux was selected as the primary cybersecurity and ethical hacking environment because it contains numerous tools used for security testing and network analysis.

Status: ✅ Completed

Screenshot

«Add your screenshot here.»

"![Kali Linux Virtual Machine](screenshots/kali-vm.png)"

---

Step 5: Configure the Kali Linux IP Address

After importing Kali Linux, I configured its network settings to operate within the NAT Network created in VirtualBox.

The lab configuration used the "10.0.0.0/24" network.

Example Configuration

IP Address: 10.0.0.2
Subnet Mask: 255.255.255.0
Network: 10.0.0.0/24

The IP configuration allows the Kali Linux machine to communicate with other machines connected to the same virtual network.

Status: ✅ Completed

Screenshot

«Add your screenshot here.»

"![Kali IP Configuration](screenshots/kali-ip-configuration.png)"

---

Step 6: Take a Snapshot of the Kali Linux VM

After successfully configuring Kali Linux, I created a VirtualBox snapshot of the virtual machine.

The snapshot provides a restore point that can be used to return the VM to its working state if the system is modified or damaged during cybersecurity practice.

Status: ✅ Completed

Screenshot

«Add your screenshot here.»

"![Kali Linux Snapshot](screenshots/kali-snapshot.png)"

---

🔹 PHASE 2: Additional Virtual Machines

Step 7: Install Additional Virtual Machines

The next stage involved downloading and installing additional virtual machines for cybersecurity practice.

The lab instructions included:

- Windows 11
- Windows 10
- Windows 7
- Android 9x

These virtual machines are intended to provide different targets and operating environments for cybersecurity and ethical hacking exercises.

Status: ✅ Completed / In Progress

Screenshot

«Add screenshots of the virtual machines you configured here.»

"![Additional Virtual Machines](screenshots/additional-vms.png)"

---

🌐 Network Connectivity Testing

After configuring the virtual machines, I performed connectivity tests using the "ping" command.

The purpose of the test was to verify that the machines could communicate successfully over the configured virtual network.

Example

ping <target-ip-address>

A successful response indicates that network connectivity between the machines is working.

Screenshot

«Add your ping test screenshot here.»

"![Network Connectivity Test](screenshots/ping-test.png)"

---

🔐 Lab Network Architecture

The cybersecurity lab uses a virtualized network environment similar to the following:

                    Host Computer
                         |
                    VirtualBox
                         |
                  NAT Network
                  10.0.0.0/24
                         |
          +--------------+--------------+
          |              |              |
        Kali          Windows        Android
       Linux             VM             VM
    10.0.0.2/24

This setup provides an environment where cybersecurity and ethical hacking exercises can be performed without directly exposing the practice machines to the production network.

---

⚠️ Challenges Encountered

During the setup, I encountered challenges related to:

- Installing and configuring virtual machines.
- Configuring the VirtualBox network.
- Assigning the correct IP configuration.
- Ensuring that the virtual machines could communicate with each other.
- Managing VM resources such as RAM and storage.

I resolved these challenges by reviewing the lab instructions, checking the VirtualBox configuration, and testing network connectivity.

---

📚 Lessons Learned

Through this lab, I learned how to:

1. Install and use Oracle VirtualBox.
2. Create a NAT Network.
3. Configure virtual machine networking.
4. Install and configure Kali Linux.
5. Assign IP addresses to virtual machines.
6. Test network connectivity using "ping".
7. Create and manage virtual machine snapshots.
8. Build an isolated environment for cybersecurity and ethical hacking practice.

---

🏁 Conclusion

The Week 1 Cybersecurity Lab Setup provided a practical foundation for future cybersecurity and ethical hacking exercises.

The virtual environment makes it possible to safely practice networking, vulnerability assessment, penetration testing, and other cybersecurity techniques using isolated virtual machines.

This setup will serve as the foundation for subsequent Networkwalks cybersecurity labs and practical exercises.

---

👤 Author

Peter Oduor

Networkwalks B082 — Week 1

Cybersecurity & Ethical Hacking Practice

---

📸 Screenshots

All screenshots documenting the lab setup should be stored in the "screenshots" folder and referenced in this README.

Recommended structure:

networkwalks-B082-week1-Cybersecurity-lab-setup/
│
├── README.md
│
└── screenshots/
    ├── 7zip-installation.png
    ├── virtualbox-installation.png
    ├── nat-network.png
    ├── kali-vm.png
    ├── kali-ip-configuration.png
    ├── kali-snapshot.png
    ├── additional-vms.png
    └── ping-test.png
