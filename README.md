# Firewall-stimulation-DSA
This report describes the deployment and configuration of a virtual firewall system to simulate enterprise network security. 
Virtual Firewall Simulation

## Report Summary  
This report describes the deployment and configuration of a virtual firewall system to simulate enterprise network security. The firewall was configured to manage internal traffic, apply custom rules, and monitor for suspicious activity. An attacker machine was used to test rule enforcement and intrusion detection capabilities. This project illustrates network segmentation, policy enforcement, and log-based traffic analysis.

### Project Overview  
This project involved configuring a firewall in a controlled lab environment to simulate the types of rule sets and monitoring processes used in real-world organizations.

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

1.### Firewall Setup  
- Installed and launched firewall appliance  
- Configured interfaces for internal and external segments  
- Assigned static IPs to internal machines

2.### Network and Device Configuration  
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

Network Diagram  
Insert diagram showing attacker, firewall, and LAN components

Screenshots  
Insert screenshot of rule setup page  
Insert screenshot of blocked SSH attempt  
Insert screenshot of real-time log monitor

Project Folder Structure  
firewall-simulation  
├── Configs  
├── Logs  
├── Screenshots  
├── firewall-rules.md  
├── README.md  
├── simulation-log.md

Outcomes  
- Built and tested a functioning firewall in virtual lab  
- Demonstrated understanding of rule-based access control  
- Simulated real-world attacks and interpreted logs  
- Applied concepts of network security segmentation

References  
Include configuration references and firewall documentation used
