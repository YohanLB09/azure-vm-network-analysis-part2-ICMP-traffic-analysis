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
After inserting your credentials and pressing "OK", you should see this pop-up window appearing on your screen. Don't worry, this is normal as the remote computer (the Windows VM) is using a self-signed Remote Desktop Protocol (RDP) certificate, which is not automatically trusted by your local machine. You can go ahead and press "Yes" to connect to the VM since we have created it in Azure.
</p>
<br />


<p>
<img src="https://i.imgur.com/Vtkde9D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
-Once the session is initated, you should see this loading screen appearing. This indicates that you are officially connected to the Windows VM. 
  
-Additionally, before reaching the Windows VM desktop, you may be asked to configure certain features/options. These are not important for the purpose of this lab so you can leave them as disabled or manually disable them.
</p>
<br />


<h3>Step 2: Install Wireshark</h3>
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
