<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" height="70%" width="70%" alt="Traffic Examination"/> 
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark and experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>Setting up the VM</h2>

**Note** *Please go to my other Repository ["Creating Virtual Machines and Accessing via Remote Desktop"](https://github.com/AbrahamMedelMorales/Creating-VMs-and-Accessing-via-Remote-Desktop) if you are not familiar with creating Virtual Machines or connecting to them via Remote Desktop.*

1. Go to [Azure's Portal](https://portal.azure.com/#home) and create a new Resource Group. We will be placing both Windows and Linux VM in this Resource Group.<br>

2. Create a Windows 10 Virtual Machine in the Resource Group you created. Create your username and password, confirm that you have an eligible Windows 10/11 license, and move onto the Network tab at the top of the **"Create a Virtual Machine page"**
<p align="center">
<img src="https://i.imgur.com/iU9sfDR.png" height="70%" width="70%" alt="Create a Virtual Machine Page"/> 
</p>
3. Create and name your new Virtual Network.
<p align="center">
<img src="https://i.imgur.com/RTL5Atx.png" height="70%" width="70%" alt="Create New Virtual Network"/> 
</p>
4. Review and Create your Windows Virtual Machine. <br>

5. Create a Linux VM in the same Resource Group as the Windows VM. Create a username and password and move to the Network tab at the top of the **"Create a Virtual Machine page"** <br>

7. Select the Virtual Network you just created from the dropdown menu.
<p align="center">
<img src="https://i.imgur.com/LXdI3k1.png" height="70%" width="70%" alt="Virtual Network from Dropdown Menu"/> 
</p>

**"Note:"** It may take a few minutes and several refresh attempts for the Virtual Network to appear as an option in the dropdown menu." <br>

<h2>Installing Wireshark into our Windows VM</h2>

1. Start your Windows VM and open up a web browser.

2. Head to [Wireshark](www.wireshark.org) and download **"Wireshark x64"**

<p align=center>
<img src="https://i.imgur.com/RDHGIkM.png" height="70%" width="70%" alt="Download WireShark"/>
</p>

3. Install Wireshark. (Click through the installation without changing any of the settings)

<p align=center>
<img src="https://i.imgur.com/CFbolrt.png" height="70%" width="70%" alt="Install Wireshark"/>
</p>



<p align=center>
<img src="" height="70%" width="70%" alt=""/>
</p>
<p>

<br />
