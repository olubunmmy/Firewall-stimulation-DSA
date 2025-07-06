# Project Title: Network Security Simulation with a Virtual Firewall


## Project Overview

This project involved the deployment and configuration of a virtual firewall to simulate an enterprise-grade network security environment. The setup aimed to mirror real-world infrastructure by implementing network segmentation, access control policies, and intrusion detection within a controlled virtual lab. A virtual attacker machine was introduced to simulate threat scenarios such as port scanning and unauthorized access attempts.

The firewall was configured with enterprise-relevant rule sets, and traffic was monitored and analyzed using built-in logging tools and external analyzers like Wireshark. This exercise reinforced core network security concepts including perimeter defense, rule enforcement, log analysis, and response validation.

---

## Objectives

- Deploy a virtual firewall in a simulated enterprise network  
- Configure LAN/WAN interfaces, IP addressing, and NAT  
- Create and enforce realistic access control rules  
- Simulate internal and external threat scenarios  
- Analyze firewall logs to assess policy effectiveness  

---

## Tools and Environment
  
- Virtual firewall appliance  
- Virtual machines for attacker and target  
- Port scanner  
- Network traffic analyzer


| Component               | Description                                      |
|-------------------------|--------------------------------------------------|
| Host OS                 | Windows 10                                       |
| Virtualization Platform | Oracle VirtualBox                                |
| Firewall Appliance      | pfSense / OPNsense (open-source enterprise firewalls) |
| Guest OS (VMs)          | Kali  (Attacker VM), Ubuntu (Target VM)         |
| Network Tools           | Nmap (port scanner), Wireshark (traffic capture) |

---

## Methodology

### 1. Enterprise Lab Setup

- Deployed Oracle VirtualBox to host isolated virtual machines
- Set up three key virtual systems:
  - **Firewall Appliance VM** (pfSense or OPNsense)
  - **Internal Target VM** (Ubuntu server)
  - **Attacker VM** (Kali with Nmap installed)
- Configured separate virtual network interfaces:
  - **LAN**: internal secure network  
  - **WAN**: public/untrusted network  
- Assigned static IPs to simulate enterprise segmentation

---

### 2. Firewall Configuration

- Accessed firewall via browser UI and configured:
  - **Interfaces**: LAN, WAN, and optional DMZ  
  - **NAT**: Enabled for internal devices to access external network  
- Created rule sets to reflect enterprise policy requirements:

| Rule Type | Interface | Source       | Destination  | Action |
|-----------|-----------|--------------|--------------|--------|
| DNS       | LAN       | Any          | External     | Allow  |
| HTTP      | LAN       | Any          | External     | Allow  |
| SSH       | WAN       | Any          | Internal     | Block  |
| ICMP      | WAN       | Any          | Firewall     | Block  |

---

### 3. Threat Simulation 

- **Simulated port scanning** from attacker VM using Nmap:
  ```bash
  nmap -sS 192.168.10.10


- Attempted unauthorized SSH access to internal system

- Used Wireshark on attacker and target machines to capture live traffic

- Verified which actions were logged, blocked, or passed

### Log Monitoring and Policy Review
- Accessed the firewall's system logs and live traffic monitor

- Reviewed alerts, timestamps, and flagged IPs

- Verified expected behavior:

- Allowed DNS and HTTP traffic from LAN

- Blocked unauthorized SSH from WAN

- Detected and logged port scanning attempts



### Results and Outcomes
- Successfully deployed a firewall in a virtual lab

- Demonstrated effective network segmentation and traffic control

- Simulated real-world attack vectors in a safe environment

- Verified rule enforcement via log review and traffic capture

- Strengthened understanding of firewall deployment, intrusion detection, and incident response

### Key Skills Demonstrated
- Deployment of open-source enterprise-grade firewall appliances

- NAT configuration, interface setup, and access control

- Hands-on penetration testing using Nmap

- Log correlation and incident verification

- Use of Wireshark for network packet inspection

- Enterprise-level rule design and policy enforcement

### Conclusion
This simulation successfully mirrored key aspects of enterprise network security by deploying a functional virtual firewall and evaluating its effectiveness under simulated attack conditions. By configuring rule sets, enforcing security policies, and analyzing logs, the project reinforced foundational cybersecurity practices used in real corporate environments.

This experience further developed my ability to implement and evaluate perimeter defenses, a crucial skill set for roles in network security, system administration, and SOC operations. The project integrates lessons from previous lab exercises and continues to build a hands-on cybersecurity portfolio aligned with industry standards.






