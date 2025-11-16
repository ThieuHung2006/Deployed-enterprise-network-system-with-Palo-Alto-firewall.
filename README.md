# Enterprise Network Deployment with Palo Alto Firewall

## Project Overview
This project demonstrates the deployment of an enterprise network using a Palo Alto firewall. It includes network segmentation into DMZ, Office, and Local zones to secure Web and DB servers and ensure controlled Internet access.

## Network Diagram
![Network Diagram](https://github.com/user-attachments/assets/7bfed913-d4be-432f-aeab-94789aac84e0)
*Diagram shows zones, routers, firewall, servers, and PCs.*

## Device Configuration Summary

### Palo Alto Firewall
- Interfaces:
  - eth1/1 → Office Zone
  - eth1/2 → Web Zone
  - eth1/3 → DB Zone
- Policies: control inter-zone traffic (DMZ cannot access Local Zone), allow necessary traffic, NAT to Internet
- IP Routes: configured as needed for inter-zone connectivity

### SW_core
- Connects Office Zone to Palo Alto firewall with static IP routes

### Servers & PCs
- Web & DB servers: static IP, ping test
- Office PCs: access Web & DB servers according to policies

## Results / Demo
- Successful ping between zones according to firewall policies
- Office/Local PCs can successfully ping devices in both Local and DMZ zones
- Devices in DMZ cannot ping Local Zone, ensuring network segmentation and security
- Internet traffic is successfully NATed through the Palo Alto firewall

## Lessons Learned
- Gained hands-on experience configuring Palo Alto firewall for inter-zone traffic control and NAT
- Learned how to design network segmentation with DMZ, Office, and Local zones to improve security
- Practiced configuring routers, static routes, and IP addressing for enterprise network topology
- Understood how to test connectivity and verify firewall policies using ping and access checks
- Developed skills in documenting network design, configuration, and results for professional reporting

## Conclusion
The project successfully demonstrates enterprise network deployment with Palo Alto firewall. Network segmentation and firewall policies ensure security, controlled access, and proper Internet connectivity.

## About
Enterprise network deployment with Palo Alto firewall, including DMZ, Office, and Local zones.
