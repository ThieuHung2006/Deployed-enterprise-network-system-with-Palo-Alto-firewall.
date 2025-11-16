# Deployed-enterprise-network-system-with-Palo-Alto-firewall.

Project Overview
This project demonstrates the deployment of an enterprise network using a Palo Alto firewall. It includes network segmentation into DMZ, Office, and Local zones to secure Web and DB servers and ensure controlled Internet access.


Network Diagram <img width="1504" height="688" alt="firewall" src="https://github.com/user-attachments/assets/7bfed913-d4be-432f-aeab-94789aac84e0" />

Device Configuration Summary:
Palo Alto Firewall
- Interfaces:
  - eth1/1 → Office Zone
  - eth1/2 → Web Zone
  - eth1/3 → DB Zone
- Policies: control inter-zone traffic (DMZ cannot access Local Zone), allow necessary traffic, NAT to Internet
SW_core
- Connects Office Zone to Palo Alto firewall with static IP routes
Servers & PCs
- Web & DB servers: static IP, ping test
- Office PCs: access Web & DB servers according to policies

Results / Demo:
- Successful ping between zones according to firewall policies
- Office/Local PCs can successfully ping devices in both Local and DMZ zones
- Devices in DMZ cannot ping Local Zone, ensuring network segmentation and security
- Internet traffic is NATed through the Palo Alto firewall

