<p align="center">
<img src="https://i.imgur.com/yGtOeVI.jpeg" alt="Basic Home SOC Lab Steps"/>
</p>

<br>
<h1>Building a Basic Home SOC Lab for Threat Detection and Analysis</h1>



<h2>Project Description</h2>
This project details the setup of a fundamental Security Operations Center (SOC) lab environment utilizing VirtualBox. The lab integrates a Kali Linux virtual machine (VM) for simulating attacks and a Windows 10 VM configured with Sysmon and Splunk for advanced log collection and centralized security information and event management (SIEM) capabilities. The objective is to demonstrate the process of launching a simulated attack (using Nmap, msfvenom, and Metasploit) to establish a reverse TCP shell, interpret detailed telemetry via Sysmon, and analyze attack patterns and behaviors within Splunk to understand real-time detection opportunities. This project showcases practical skills in cybersecurity lab setup, offensive security simulation, and defensive security analysis.



<h2>Environments and Technologies Used</h2>

- <b>Virtualization:</b> VirtualBox
- <b>SIEM:</b> Splunk Enterprise
- <b>Endpoint Telemetry:</b> Sysmon
- <b>Offensive Security Tools:</b> Nmap, Msfvenom, Metasploit Framework



<h2>Operating Systems Used</h2>

- <b>Kali Linux VM:</b> Used as the attacker machine, hosting offensive security tools.
- <b>Windows 10 VM:</b> Configured as the victim machine, with security tools for log generation and aggregation.



<h2>Overview of Steps</h2>
1. <b>Virtual Machine Setup:</b> Creation of isolated Kali Linux and Windows 10 VMs within VirtualBox to establish a sandboxed lab environment.
<br>
2. <b>Defensive Tool Deployment:</b> Installation and configuration of Sysmon and Splunk on the Windows 10 VM for comprehensive log aggregation and analysis.
<br>
3. <b>Offensive Simulation:</b> Utilization of msfvenom, Metasploit, and Nmap to generate a malware payload, establish a reverse TCP shell connection, and conduct network scanning to generate security logs.
<br>
4. <b>Log Ingestion and Analysis:</b> Configuration of Splunk to ingest Sysmon-generated logs, followed by analysis of these logs to identify and interpret attack patterns.



<h2>Project Walkthrough</h2>
<p>
<h3> Step 1: Virtual Machine Setup </h3>

1. Download VirtualBox and its associated hash file. Verify the integrity of the downloaded VirtualBox installer by comparing its SHA256 hash with the one provided on the official VirtualBox website. This confirms that the file was not corrupted during transit. <br>
<img src="https://i.imgur.com/C0JCgwB.png" alt="Disk Sanitization Steps"/>
<br>
<img src="https://i.imgur.com/4a3jLg3.png" alt="Disk Sanitization Steps"/>
<br>
2. Install VirtualBox. Prepare the Windows 10 virtual machine by installing the Windows ISO file.
<br>
<img src="https://i.imgur.com/rYoTIzL.png" alt="Basic Home SOC Lab Steps"/>
<br />
3. Configure the Windows 10 VM settings, including assigning 5120 MB of base memory and 4 processors (Always remember to choose your memory and processor settings according to your system capacity). Set the network adapter to "Internal Network" with the name 'mytest' to ensure a sandboxed environment.
<br>
<img src="https://i.imgur.com/617njbE.png" alt="Basic Home SOC Lab Steps"/>
<br />

</p>
