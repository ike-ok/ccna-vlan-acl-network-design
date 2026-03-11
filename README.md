# ccna-vlan-acl-network-design
Network Design for a 100 user Bank

Project Title
Enterprise VLAN Segmentation with ACL Security

Overview
This project demonstrates VLAN segmentation, DHCP configuration, inter-VLAN routing, and access control lists implemented in Cisco Packet Tracer.

Technologies
Cisco IOS, VLANs, Router on a Stick, DHCP, Extended ACLs, Trunking (802.1Q)

Network Design
5 departmental networks were created:

VLAN: 10
Department: Customer Service
Subnet:192.168.28.0 /26

VLAN: 20
Department: Loans
Subnet: 192.168.28.64 /27

VLAN: 30
Department: Marketing
Subnet: 192.168.28.96 /27

VLAN: 40
Department: Sales
Subnet: 192.168.28.128 /27

VLAN: 50
Department: IT
Subnet: 192.168.28.160 /28

Security Policy
The following access control policy was implemented:
-Customer Service is not allowed access to any other subnet
-No other department subnet is allowed to access IT's subnet
-Inter-VLAN routing is handled by router subinterfaces

Key Configurations
Access-list 100 deny ip any 192.168.28.160 0.0.0.15
access-list 100 deny ip 192.168.28.0 0.0.0.63 192.168.28.64 0.0.0.63 
access-list 100 deny ip 192.168.28.0 0.0.0.63 192.168.28.128 0.0.0.63  

Features Demonstrated
-VLAN segementation
-Inter-VLAN routing
-DHCP configuration
-Extended ACL filtering
-Network security policy enforcement
