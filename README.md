# Network-Intrusion-Detection-System-Using-Snort
Using Snort to detect and prevent network-based attacks in real-time

Abstract. This project focuses on implementing a Network Intrusion Detection System (NIDS) using Snort to detect and prevent network-based attacks. The primary goal was to detect and prevent network-based attacks in real time. The system was tested in a virtual environment using Kali Linux as the attacking machine and Ubuntu as the monitored system. Through various attack simulations, Snort successfully detected malicious activities in real-time. This project highlights Snort’s effectiveness in providing real-time intrusion detection and the importance of adapting rules to specific network services for protection.

# Objectives:

Setup Snort on an Ubuntu machine and configure it to monitor a designated network

Simulate attacks using information gathering tools Nmap and Legion from Kali Linux

Evaluate the performance and accuracy of Snort in detecting these attacks

# Part I: Setup

The project environment was built using two virtual machines, Kali Linux as the attacking machine and Ubuntu as the monitored machine. Snort was installed on the Ubuntu machine and the network interface card on the Ubuntu machine was configured to be in promiscuous mode to ensure that all network traffic could be monitored. The setup involved installing and configuring Snort on a network interface card, adjusting the home network variables, and defining specific rules to monitor for various types of attacks.

![Screenshot 2024-09-25 203527](https://github.com/user-attachments/assets/3a5a31d0-6d45-4007-8713-7cd5a4e8b887)

_Figure 1.1: IP address and Network Interface Card for Ubuntu_

![Screenshot 2024-09-25 203634](https://github.com/user-attachments/assets/ed09d6d8-287b-4317-b326-063cb24f12a7)

_Figure 1.2: Verifying attacking machine IP address_

Before running Snort, the configuration file was reviewed and tests were conducted to validate the setup. Snort was configured to monitor traffic on the home network and log activity to a centralized logging system.

![Screenshot 2024-09-25 210540](https://github.com/user-attachments/assets/8f926a06-dec9-4a8a-a083-c8855dd5e06c)

_Figure 1.3: Snort successfully validated the configuration_

# Part II: Attack Simulation and Detection

Once the environment was configured and Snort validated, the next step involved attack simulation from the Kali Linux machine.

![Screenshot 2024-09-25 210831](https://github.com/user-attachments/assets/b9ec2799-62da-4854-b0f1-6b8e59f32cff)

_Figure 2.1: Monitoring enabled_

Going back to the Kali attack machine, an Nmap scan was initiated from the Kali Linux machine targeting the Ubuntu machine. The goal of this simulation was to test Snort’s capability in detecting basic reconnaissance.

A full network scan using Nmap was executed, sending multiple probes to detect open ports, running services, and system fingerprints.

![Screenshot 2024-09-25 211021](https://github.com/user-attachments/assets/e49f3c87-5c34-4b94-8f7b-a89fb922fb18)

_Figure 2.2: Nmap scan_

Snort successfully detected the scan and generated alerts.

![Screenshot 2024-09-25 211030](https://github.com/user-attachments/assets/330a3b04-ebb4-48e9-b57d-077d40ed7a97)

Figure 2.3: Snort detecting the Nmap scan

Legion is another tool for information gathering. This tool was employed to simulate more advanced reconnaissance and network mapping attacks. Using Legion, the IP address of the Ubuntu machine was scoped, and detailed scans were performed.

The attack targeted different services running on the Ubuntu machine, attempting to map open ports and exploit known vulnerabilities.

![Screenshot 2024-09-26 182332](https://github.com/user-attachments/assets/7581cea5-3d67-4eaa-a0c6-91cfb368d5c0)

_Figure 2.4: adding Ubuntu machine IP address to scope_

Snort was again successful in detecting these malicious activities and issued real-time alerts.

![Screenshot 2024-09-26 182451](https://github.com/user-attachments/assets/e29c6977-57e0-43ad-bb2d-a9029d8ba209)

_Figure 2.5: Snort detecting Legion scanning attack_






