# Create-A-Windows-Domain-Virtual-Network-in-VMware
Welcome to my VMware lab. The purpose of this project is to create a homelab network primarily in VMware. Throughout this lab i will explore using Active Directory, setting up a Windows Domain Controller, exploring DNS, DHCP. The network will be set up so it be scaled as needed. 

# Windows Server 2022 Domain Controller
As mentioned above our domain controller will be Windows Server. Specifically Windows Server 2022, the Domain Controller will be set up for Load Balancing. DNS and DHCP will be set up on seperate Windows Server isos.

# Firewall and Routing
For Firewall and Routing we will use pfsense. Using the WAN interface pfsense will set up to NAT from the homelab network of 10.11.0.0 /16 to home network for internet connection. This interface will also act as our default gateway.

# VLANS
3 LAN interfaces will be set up for now and 2 VLAN. The first LAN interface will contain a Rocky Linux desktop that's only purpose is to access the pfsense web console. VLAN 5 (10.11.5.1) which it have all the Servers assigned to it. VLAN 10 (10.11.10.1) will have the clients.
