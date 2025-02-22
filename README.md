# Azure VM Network Analysis - Part 2 - ICMP Traffic Analysis

In this tutorial, we will observe ICMP network traffic between two Azure Virtual Machines using Wireshark and PowerShell.

<p align="center">
<img src="https://i.imgur.com/Gfc6Ipg.png" alt="Traffic Examination"/>
</p>


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop 
- PowerShell 
- Network protocol (ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 Pro, version 22H2
- Ubuntu Server 22.04 LTS

<h2>High-Level Steps</h2>

- Step 1: Connect to the Windows Virtual Machine
- Step 2: Install Wireshark
- Step 3: Filter for ICMP traffic and observe
- Step 4: Prepare for Part 3

<h2>Actions and Observations</h2>

<h3>Step 1: Connect to the Windows Virtual Machine</h3>
<p>
<img src="https://i.imgur.com/4xl480l.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Select your Windows VM and copy its Public IP address. 
</p>
<br />


<p>
<img src="https://i.imgur.com/NCbzwRc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Type Remote Desktop Connection in the search bar and click on "Open".
</p>
<br />


<p>
<img src="https://i.imgur.com/jtXUYuE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Paste the Windows VM Public IP address in Remote Destop Connection and click on "Connect".
  
-In the new pop-up window, enter the Windows VM password (the one created in Part 1) and click on "OK" to initiate the session.
</p>
<br />


<p>
<img src="https://i.imgur.com/XsmfHbI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-After inserting your credentials and pressing "OK", you should see this pop-up window appearing on your screen. Don't worry, this is normal as the remote computer (the Windows VM) is using a self-signed Remote Desktop Protocol (RDP) certificate, which is not automatically trusted by your local machine. You can go ahead and press "Yes" to connect to the VM since we have created it in Azure.
</p>
<br />


<p>
<img src="https://i.imgur.com/Vtkde9D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Once the session is initated, you should see this loading screen appearing. This indicates that you are officially connected to the Windows VM. 
  
-Additionally, before reaching the desktop, you may be asked to configure certain features/options. These are not important for the purpose of this lab so you can leave them as disabled or manually disable them.
</p>
<br />


<h3>Step 2: Install and run Wireshark</h3>
<p>
<img src="https://i.imgur.com/sqtRiCZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Use the Microsoft Edge app on the desktop and go to www.wireshark.org.
  
-Click on "Download".
</p>
<br />


<p>
<img src="https://i.imgur.com/ZgCC1Gq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Download the Windows x64 installer version. 
  
-Once the download is completed, click on "Open file" and you should see the installation pop-up window appearing. 

-Follow along the Wizard while leaving all the default configuration as they are and complete the installation process.
</p>
<br />

<h3>Step 3: Filter for ICMP traffic and observe</h3>
<p>
<img src="https://i.imgur.com/9KIg9Xj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Open Wireshark and click on "Ethernet" to select the Ethernet network adapter, it should become highlighted.
  
-Click on the shark fin in the upper left to start the packet capture.
</p>
<br />


<p>
<img src="https://i.imgur.com/jEjetaJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-You will notice a high amount of traffic occurring. This is expected due to normal network operations, background processes, and Azure-related activity. 
  
-While the packet capture is still running, type "icmp" in the search bar and press "Enter" to filter for ICMP traffic. You will observe that there are no such traffic currently happening which is normal since no device has tried to initiate a ping request to the Windows VM or vice-versa.
</p>
<br />


<p>
<img src="https://i.imgur.com/WjzlWrP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Go back to Azure, select the Linux VM, click on "Network settings" and copy the Linux VM Private IP address.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
