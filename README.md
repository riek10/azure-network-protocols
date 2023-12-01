<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Network Protocols (SSH,ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Install Wireshark
- Filter through ICMP traffic ONLY / Deny ICMP Traffic 
- Filter through SSH traffic ONLY/ Capture command traffic on wireshark

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
<img src="https://github.com/riek10/azure-network-protocols/assets/113129662/f3cc355e-7cce-4ced-8680-93a5ed18b738" height="50%" width="50%"/>
<img src="https://github.com/riek10/azure-network-protocols/assets/113129662/3ee8585a-8172-443f-86d9-a1791956e5a9" height="50%" width="50%"/>
</p>
<p>
In this final step im filtering through ONLY SSH traffic on wireshark and typing a few commmands on the UBUNTU VM to see what response i would receive on wireshark. I was extremely interested in the results of this step because ive completed countless labs and personal projects using Linux OS and not once did i considered observing the findings from a connection between Linux and Windows. In the two screenshots above you can see the successfull SSH into the Linux machine and you can see wireshark capturing the traffic between the two machines.
</p>
<br />
