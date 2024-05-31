<p align="center">
<img src="https://i.imgur.com/6xuIYna.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>ANALYZING NETWORK TRAFFIC USING WIRESHARK</h1>
In this project, I explored the configuration and connectivity of two virtual machines hosted on Microsoft Azure, one running Windows 10 and the other on a Linux operating system. Both machines were organized within the same resource group, AD-LAB, and utilized a shared virtual network named VM1-vnet. My objective was to analyze network behaviors and configurations extensively using various tools and commands. I accessed the Windows VM via Remote Desktop Protocol (RDP) to install Wireshark, a sophisticated network protocol analyzer, which allowed me to capture and inspect network traffic. I conducted a series of network tests including ICMP pinging, adjusting firewall settings, SSH connectivity, and DNS lookups to amazon.com and facebook.com. These activities helped to deepen my understanding of network protocols and security settings within a cloud environment.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- PowerShell

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu 20.4

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1:
 I set up two Azure virtual machines, one running Windows 10 and the other running Linux. Both are organized under the same resource group named AD-LAB and share a virtual network called VM1-vent.
- <img src="https://i.imgur.com/cyNFPtC.png" alt="Microsoft Active Directory Logo"/>
- Step 2:
 I used Remote Desktop Protocol (RDP) to access my Windows VM, where I downloaded Wireshark, a network protocol analyzer.
  <img src="https://i.imgur.com/o95g8Z0.png" alt="Microsoft Active Directory Logo"/>
- Step 3:
- To check the connectivity of my Linux VM,On my Windows 10 VM PowerShell, I used the ping command to send ICMP packets to its private IP address, 10.0.0.5. I then filtered for ICMP in Wireshark to analyze the packet exchange.
- <img src="https://i.imgur.com/rYekHg0.png" alt="Microsoft Active Directory Logo"/>
- Step 4:
 I returned to the network security group (firewall) settings of my Linux VM. I created an inbound rule to block ICMP traffic and observe the effects on connectivity, resulting in connectivity timeout and packet loss.
- <img src="https://i.imgur.com/PErEHsW.png" alt="Microsoft Active Directory Logo"/>
- <img src="https://i.imgur.com/XlKBSK8.png" alt="Microsoft Active Directory Logo"/>
- Step 5:
 After observing the effects of blocking ICMP traffic, I modified the inbound rule in the network security group settings for my Linux VM to allow ICMP traffic again. Then, I conducted a continuous ping to further monitor the echo requests and responses.
- <img src="https://i.imgur.com/49MktQd.png" alt="Microsoft Active Directory Logo"/>
- <img src="https://i.imgur.com/M4XRDcs.png" alt="Microsoft Active Directory Logo"/>

-  Step 6:
-  Furthermore, I used SSH (Secure Shell Protocol) to remotely access my Linux VM, allowing me to analyze the network connection in more detail.
-  <img src="https://i.imgur.com/auEcVXp.png" alt="Microsoft Active Directory Logo"/>
-  Step 7:
-  I ran the nslookup command to query the DNS records for amazon.com and facebook.com, observing the responses to understand the DNS protocol behavior.
-  <img src="https://i.imgur.com/ksyPXUZ.png" alt="Microsoft Active Directory Logo"/>

<h2>CONCLUSION</h2>
I set up two virtual machines on Azure, one running Windows 10 and the other Linux, both under the same resource group named AD-LAB and sharing a virtual network called VM1-vent. I accessed the Windows VM via RDP to download and use Wireshark, a network protocol analyzer. To test the network connectivity of the Linux VM, I used the ping command to send ICMP packets to its private IP address, 10.0.0.5 and monitored the exchange with Wireshark. Observing the effects of network settings, I adjusted the Linux VM's network security group (firewall) to initially block and then allow ICMP traffic, conducting a continuous ping to further analyze the echo requests and responses. Additionally, I utilized SSH to remotely connect to the Linux VM for a deeper analysis of the network connection. I also employed the nslookup command to query DNS records for amazon.com and facebook.com, gaining insights into DNS protocol responses. This comprehensive setup and testing provided valuable information on network configurations and behaviors across both virtual machines.



