<h1>Virtual Private Cloud Configuration</h1>


<h2>Description</h2>


This project focuses on creating and configuring a Virtual Private Cloud (VPC) environment using a cloud provider's management console, AWS. The goal is to gain hands-on experience in designing secure, isolated network infrastructure for deploying cloud-based applications. The setup process includes defining VPC components such as subnets, route tables, and internet gateways, and configuring security groups and network access control lists (ACLs) to enforce security policies. Additionally, the project involves deploying a virtual machine within the VPC to simulate application hosting and testing connectivity and security configurations. By completing this project, I can demonstrate proficiency in setting up a secure and functional VPC environment and gain skills in network segmentation, resource isolation, and security enforcement in cloud-based infrastructures.
<br />


<h2>Languages and Utilities Used</h2>

- <b>AWS Management Console</b> 
- <b>Networking Components (e.g., Subnets, Route Tables, Security Groups, Network ACLs)</b>
- <b>Virtual Machine Instances (Amazon Linux)</b>
- <b>OpenSSH (for secure shell access to virtual machines)t</b>
   
<h2>Environments Used </h2>

- <b>Operating System: Amazon Linux</b> (deployed on a virtual machine within the VPC)
- <b>Network Environment:A cloud-based Virtual Private Cloud (VPC) setup, including subnets, route tables, internet gateways, and security groups to simulate an isolated and secure network environment
- <b>Development/Testing Tools: AWS Management Console for VPC and resource configuration, AWS EC2 for deploying the Amazon Linux instance, and SSH for secure access and configuration
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
