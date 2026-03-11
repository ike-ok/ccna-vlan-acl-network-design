

<h1> Enterprise VLAN Segmentation with ACL Security for a 100 User Bank </h1> 


<h3> Overview </h3>

This project demonstrates VLAN segmentation, DHCP configuration, inter-VLAN routing, and access control lists implemented in Cisco Packet Tracer.

<h3> Technologies </h3>

Cisco IOS, VLANs, Router on a Stick, DHCP, Extended ACLs, Trunking (802.1Q)

<h3> Network Design </h3>

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

<h3> Security Policy </h3>
The following access control policy was implemented: <br>

<ul>
<li> Customer Service is not allowed access to any other subnet </li>
<li> No other department subnet is allowed to access IT's subnet </li>
<li> Inter-VLAN routing is handled by router subinterfaces </li>
</ul>

<h5> Key Configurations </h5>
<ul> 
  <li> access-list 100 deny ip any 192.168.28.160 0.0.0.15 </li>
<li> access-list 100 deny ip 192.168.28.0 0.0.0.63 192.168.28.64 0.0.0.63 </li> 
<li> access-list 100 deny ip 192.168.28.0 0.0.0.63 192.168.28.128 0.0.0.63 </li>  
</ul>

<h3> Features Demonstrated </h3>

<ul> 
  <li> VLAN segementation </li>
<li> Inter-VLAN routing </li>
<li> DHCP configuration </li>
<li> Extended ACL filtering </li>
<li> Network security policy enforcement </li>
</ul>
