# azure-network-protocols
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

- Initiate a network ping to virtual machine
- Observe network traffic
- Use wireshark to filter and capture icmp traffic
- Use wireshark to filter and capture ssh traffic

<h2>Actions and Observations</h2>

<p>
<img src=https://i.imgur.com/Kya2t9d.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Initiating a network ping to virtual machine: To initiate a network ping to a virtual machine (VM), first ensure that the VM is powered on and connected to the network. On your local machine, open the Command Prompt (Windows) or Terminal (Linux/macOS). Type the command `ping <IP_address>` where `<IP_address>` is the network IP address of the virtual machine you want to ping. Press Enter. If the network connection is properly configured, you should see a series of replies from the VM, indicating that the network communication is successful. If there is no response, check the VM's network settings, firewall configurations, and ensure it is reachable on the same network or subnet.</h2>
</p>
<br />

<p>
<img src=https://i.imgur.com/K6tFcJo.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Use wireshark to filter and capture icmp traffic: To use Wireshark to filter and capture ICMP traffic, first open Wireshark and select the network interface you want to monitor. Once the interface is selected, start the capture by clicking the "Start" button. To filter only ICMP traffic, type `icmp` into the filter bar at the top of the Wireshark window and press Enter. This will limit the capture to only ICMP packets, such as those used in ping requests and replies. You can now observe the ICMP traffic in real-time, including details such as the source and destination IP addresses, sequence numbers, and response times. To stop capturing, click the "Stop" button in the Wireshark toolbar.</h2>
</p>
<br />

<p>
<img src=https://i.imgur.com/XG4Eq6f.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Use wireshark to filter and capture ssh traffic: To use Wireshark to filter and capture SSH traffic, first open Wireshark and select the network interface you wish to monitor. Click the "Start" button to begin capturing packets. In the filter bar at the top of the window, type `tcp.port == 22` and press Enter. This filter will display only SSH traffic, as SSH typically operates over TCP port 22. As packets are captured, you will see detailed information about the SSH connections, including the source and destination IP addresses. To stop capturing, click the "Stop" button in the Wireshark toolbar. This allows you to focus specifically on the SSH traffic during your capture session.</h2>
</p>
<br />
