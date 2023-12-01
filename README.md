<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Install Wireshark
- Step 2
- Step 3
- Step 4

<h2>Actions and Observations</h2>

<p>
<img src="https://github.com/riek10/azure-network-protocols/assets/113129662/f876b1ee-d5df-499f-964c-5d51cd14b951" height="80%" width="80%"/>
</p>
<p>
To inspect the traffic and any errors that may occur on the Linux VM i configured in Azure i downloaded Wireshark which is basically an analysis tool. Once open i configured Wireshark to filter for ICMP traffic only which would enale it to only display any network communication errors.Pictured above im attempting to ping the Linux machine using its private ip address and as you can see wireshark shows the machines response.
</p>
<br />

<p>
<img src="https://github.com/riek10/azure-network-protocols/assets/113129662/48428621-01ed-465d-9b45-8e3721e4afef" height="50%" width="50%"/>
<img src="https://github.com/riek10/azure-network-protocols/assets/113129662/f6585c7a-cf25-429b-aef8-e60e78b2cbbe" height="50%" width="50%"/>
</p>
<p>
 In this step i decided to disable and inbound ICMP traffic through the Network Security Groups on Azure and if you take a look at the VM pictured above the ongoing ping to the Linux machine times out meaning it is no longer responding to the ping.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
