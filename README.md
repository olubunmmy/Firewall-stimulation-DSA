# Project Title: Enterprise-Grade Network Security Simulation with a Virtual Firewall

---

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

| Component               | Description                                      |
|-------------------------|--------------------------------------------------|
| Host OS                 | Windows 10                                       |
| Virtualization Platform | Oracle VirtualBox                                |
| Firewall Appliance      | pfSense / OPNsense (open-source enterprise firewalls) |
| Guest OS (VMs)          | Ubuntu (Attacker VM), Ubuntu (Target VM)         |
| Network Tools           | Nmap (port scanner), Wireshark (traffic capture) |

---

## Methodology

### 1. Enterprise Lab Setup

- Deployed Oracle VirtualBox to host isolated virtual machines
- Set up three key virtual systems:
  - **Firewall Appliance VM** (pfSense or OPNsense)
  - **Internal Target VM** (Ubuntu server)
  - **Attacker VM** (Ubuntu or Kali with Nmap installed)
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

### 3. Threat Simulation (Enterprise Use Case)

- **Simulated port scanning** from attacker VM using Nmap:
  ```bash
  nmap -sS 192.168.10.10


## Project Overview 
This Project report describes the deployment and configuration of a virtual firewall system to simulate enterprise network security. The firewall was configured to manage internal traffic, apply custom rules, and monitor for suspicious activity. An attacker machine was used to test rule enforcement and intrusion detection capabilities. This project illustrates network segmentation, policy enforcement, and log-based traffic analysis.



### Objectives  
- Deploy a firewall in a virtual network  
- Configure interfaces and access rules  
- Simulate unauthorized access attempts  
- Analyze and document system logs

### Tools and Environment  
- Virtual firewall appliance  
- Virtual machines for attacker and target  
- Port scanner  
- Network traffic analyzer

#### Implementation Steps  

1. Firewall Setup  
- Installed and launched firewall appliance  
- Configured interfaces for internal and external segments  
- Assigned static IPs to internal machines

2. Network and Device Configuration  
- Configured attacker machine on same internal network  
- Target system positioned on LAN segment  
- Verified routing and IP communication

3. Rule Creation and Testing  
Rule         Interface    Source    Destination    Action  
DNS          LAN          Any       External       Allow  
SSH          WAN          Any       LAN            Block  
HTTP         LAN          Any       External       Allow

4. Attack Simulation  
- Performed port scan from attacker system  
- Attempted brute-force on SSH  
- Observed rule enforcement in firewall logs

5. Log Analysis  
- Opened firewall logs to identify traffic attempts  
- Verified detection of blocked and allowed actions  
- Assessed effectiveness of rule configuration



Screenshots  
Insert screenshot of rule setup page  
Insert screenshot of blocked SSH attempt  
Insert screenshot of real-time log monitor


Outcomes  
- Built and tested a functioning firewall in virtual lab  
- Demonstrated understanding of rule-based access control  
- Simulated real-world attacks and interpreted logs  
- Applied concepts of network security segmentation


