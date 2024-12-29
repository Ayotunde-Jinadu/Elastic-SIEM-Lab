<h1>Elastic SIEM Lab</h1>


<h2>Description</h2>

This project focuses on building a home lab environment for Elastic Stack Security Information and Event Management (SIEM) using the Elastic web portal and a Kali Linux virtual machine. The goal is to gain hands-on experience with Elastic SIEM, enabling the monitoring and analysis of security events. The setup process includes configuring the Elastic web portal, preparing a Kali Linux VM, and generating security events on the VM to simulate real-world scenarios. An agent is installed and configured on the Kali VM to forward event data to the SIEM. Once data is ingested, logs are queried and analyzed directly within the Elastic SIEM interface to identify and investigate potential security issues. This project demonstrates proficiency in deploying and utilizing Elastic Stack for security monitoring and highlights skills in system setup, event generation, and log analysis.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Bash</b> 
- <b>Elastic Stack (Elasticsearch, Kibana, and Elastic Defend)</b>
- <b>Kali Linux</b>
- <b>Elastic Agent</b>
- <b>Nmap</b>
   
<h2>Environments Used </h2>

- <b>Operating System: Kali Linux</b> (via VirtualBox on Windows 11 22H2)
- <b>Network Environment: A home lab network setup to simulate security events, with traffic forwarded from the Kali VM to the Elastic Stack for analysis</b>
- <b>Development/Testing Tools: Elastic Web Portal, VirtualBox</b>

<h2>Program walk-through:</h2>

<p align="center">
The initial step involves creating a free account on the Elastic Cloud to set up a cloud-based Elastic instance for running the SIEM. Simultaneously, a Linux virtual machine is configured using Oracle VirtualBox with Kali Linux as the operating system, providing a local environment to interact with and analyze data through the Elastic SIEM platform. This establishes both the cloud instance and the local system required for the lab. : <br/>
<img src="https://i.imgur.com/TskEBzh.png" height="80%" width="80%" 
<br />
<img src="https://i.imgur.com/timOwKb.png" height="80%" width="80%" alt="Elastic SIEM Lab Steps"/>
<br />
<br />
The Elastic Agent is installed on the Kali VM to collect and forward security-related events to the Elastic SIEM instance. This involves downloading and configuring the agent software to ensure it communicates effectively with the Elastic Cloud. After installation, the agent's status is verified using the command sudo systemctl status elastic-agent.service, confirming it is active and correctly forwarding logs for analysis. This step establishes the data collection pipeline necessary for monitoring and analysis in the Elastic SIEM platform. :  <br/>
<img src="https://i.imgur.com/eFEz27F.png" height="80%" width="80%" alt="Elastic SIEM Lab Steps"/>
<br /> 
<img src="https://i.imgur.com/b9JIsYO.png" height="80%" width="80%" alt="Elastic SIEM Lab Steps"/>
<br /r>
<img src="https://i.imgur.com/rmuDxxr.png" height="80%" width="80%" alt="Elastic SIEM Lab Steps"/>
<br />
<br />
To ensure the Elastic Agent is functioning correctly, security-related events are generated on the Kali VM using Nmap, a powerful network exploration and security auditing tool. Nmap is used to scan for open ports, identify operating systems, and gather network details, creating events that the Elastic Agent forwards to the Elastic SIEM. Commands like nmap -sS <ip address>, nmap -sT <ip address>, and nmap -p- <ip address> are run to generate meaningful data. These scans produce events such as detected open ports and identified services, which validate the agent's ability to capture and forward security-relevant information. : <br/>
<img src="https://i.imgur.com/AGKwT0w.png" height="80%" width="80%" alt="Elastic SIEM Lab Steps"/>
<br />
<br />
With data successfully forwarded from the Kali VM to the Elastic SIEM, the next step is to query and analyze the logs within the SIEM platform. By examining the telemetry, you can identify and investigate security incidents, gaining insights into how threats are detected and managed. This process provides a practical understanding of security operations and incident response in real-world scenarios. :  <br/>
<img src="https://i.imgur.com/YTJYVqF.png" height="80%" width="80%" alt="Elastic SIEM Lab Steps"/>
<br />
<br />
In the Elastic SIEM, dashboards are used to visualize and analyze log data for patterns or anomalies. A custom dashboard is created to display metrics such as the count of security events over time, providing a clear and intuitive view of activity. This visualization helps in quickly identifying trends and potential security issues for more effective monitoring and analysis. :  <br/>
<img src="https://i.imgur.com/M8g4QqG.png" height="80%" width="80%" alt="Elastic SIEM Lab Steps"/>
<br />
<br />
Alerts in a SIEM are essential for identifying and responding to security incidents promptly. An alert is created in the Elastic SIEM instance to detect Nmap scans by defining a custom rule that monitors logs for scan-related events. This alert is configured to trigger notifications when specific conditions, such as detecting Nmap activity, are met. By setting up this alert, the system ensures real-time detection and response to potential security threats. :  <br/>
<img src="https://i.imgur.com/mFs03Xt.png" height="80%" width="80%" alt="Elastic SIEM Lab Steps"/>
<br />
<img src="https://i.imgur.com/AdSptpq.png" height="80%" width="80%" alt="Elastic SIEM Lab Steps"/>
<br />
<img src="https://i.imgur.com/lqSPMLd.png" height="80%" width="80%" alt="Elastic SIEM Lab Steps"/>
<br />
<img src="https://i.imgur.com/QlkAJ22.png" height="80%" width="80%" alt="Elastic SIEM Lab Steps"/>
<br />
<br />
I used Wireshark to review the captured packets and analyze the decrypted data, focusing on the SSL handshake. This allowed me to examine the traffic in various formats, providing a detailed view of the handshake process and encrypted communications. :  <br/>
<img src="https://imgur.com/EsvGkPU.png" height="80%" width="80%" alt="Network Traffic Analysis & Decryption with Logging Tool Steps"/>
<br />
<br />
Observe the decrypted data:  <br/>
<img src="https://imgur.com/e34VzbD.png" height="80%" width="80%" alt="Network Traffic Analysis & Decryption with Logging Tool Steps"/>
</p>
