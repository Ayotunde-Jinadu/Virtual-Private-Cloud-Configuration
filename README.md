<h1>Virtual Private Cloud Configuration</h1>


<h2>Description</h2>


This project focuses on creating and configuring a Virtual Private Cloud (VPC) environment using a cloud provider's management console, AWS. The goal is to gain hands-on experience in designing secure, isolated network infrastructure for deploying cloud-based applications. The setup process includes defining VPC components such as subnets, route tables, and internet gateways, and configuring security groups and network access control lists (ACLs) to enforce security policies. Additionally, the project involves deploying a virtual machine within the VPC to simulate application hosting and testing connectivity and security configurations. By completing this project, I can demonstrate proficiency in setting up a secure and functional VPC environment and gain skills in network segmentation, resource isolation, and security enforcement in cloud-based infrastructures.
<br />


<h2>Languages and Utilities Used</h2>

- <b>AWS Management Console</b> 
- <b>Networking Components (e.g., Subnets, Route Tables, Security Groups, Network ACLs)</b>
- <b>Virtual Machine Instances (Amazon Linux)</b>
- <b>OpenSSH (for secure shell access to virtual machines)</b>
   
<h2>Environments Used </h2>

- <b>Operating System: Amazon Linux</b> (deployed on a virtual machine within the VPC)
- <b>Network Environment:A cloud-based Virtual Private Cloud (VPC) setup, including subnets, route tables, internet gateways, and security groups to simulate an isolated and secure network environment
- <b>Development/Testing Tools: AWS Management Console for VPC and resource configuration, AWS EC2 for deploying the Amazon Linux instance, and SSH for secure access and configuration
<h2>Program walk-through:</h2>

<p align="center">
To get started with this project, I first created an AWS account. I visited the AWS homepage and clicked on "Create an AWS Account." During the registration process, I provided my email address, set up a secure password, and chose an account name. After that, I entered my billing information, verified my identity through a phone number and a one-time password (OTP), and selected the free-tier usage plan to minimize costs during the project. Once the setup was complete, I logged into the AWS Management Console, which served as the primary interface for configuring and managing my Virtual Private Cloud (VPC). : <br/>
<img src="https://i.imgur.com/om2BTbt.png" height="80%" width="80%" 
<br />
<img src="https://i.imgur.com/jcseDTA.png" height="80%" width="80%" alt="VPC Steps"/>
<br />
<br />
Next, I created the Virtual Private Cloud (VPC) using the AWS Management Console. I navigated to the VPC Dashboard and selected Create VPC. For the IPv4 CIDR block, I manually input 10.0.0.0/16 to define the private address range for my network. I chose to use the Amazon-provided IPv6 CIDR block to ensure my VPC was ready for modern networking requirements. After configuring the CIDR blocks, I selected the option to create a public subnet for instances that need internet access. I kept the other settings at their default values, including the selection of the Amazon Linux AMI for the operating system and the default storage configurations. This step ensured that the VPC and its associated resources were set up with minimal complexity, making it easy to focus on networking and security configurations later in the project. :  <br/>
<img src="https://i.imgur.com/16ban8C.png" height="80%" width="80%" alt="VPC Steps"/>
<br /> 
<img src="https://i.imgur.com/QodSMOT.png" height="80%" width="80%" alt="VPC Steps"/>
<br />
<br />
With the VPC in place, I proceeded to create and launch a virtual machine within it. First, I created an RSA-encrypted key pair for secure access. Using the AWS Management Console, I navigated to EC2 > Key Pairs, generated a new key pair, and downloaded the private key (.pem file) to my local machine for later use with SSH. Next, I set up a firewall security group to define the traffic rules for my virtual machine. I configured the security group to allow inbound SSH traffic (port 22) from my local IP address, ensuring secure and controlled access to the instance. All other inbound traffic was denied by default, while outbound traffic was left unrestricted. I configured the instance to run within the public subnet of my VPC, ensuring it could connect to the internet if needed. I kept the default instance type (t2.micro) to take advantage of AWS free-tier eligibility and configured the storage settings as default, which provided an 8 GB general-purpose SSD for the instance. Finally, I launched the virtual machine. Once the instance was up and running, I tested connectivity using SSH with the RSA key pair to confirm that I could securely access and manage the instance. : <br/>
<img src="https://i.imgur.com/Txj2Mf3.png" height="80%" width="80%" alt="VPC Steps"/>
<br /> 
<img src="https://i.imgur.com/3zBoN5x.png" height="80%" width="80%" alt="VPC Steps"/>
<br />
<img src="https://i.imgur.com/17JYLlj.png" height="80%" width="80%" alt="VPC Steps"/>
<br />
<br />
After successfully creating and launching the virtual machine, I reviewed and documented the instance summary to ensure everything was running correctly. Using the AWS Management Console, I navigated to the EC2 Dashboard and located my instance under the "Running Instances" section. The instance was in the "Running" state, with a public IPv4 address assigned and accessible for remote connections via SSH. It was configured as a t2.micro instance, taking advantage of AWS free-tier eligibility. The security group I had created was correctly applied, allowing inbound SSH traffic from my IP address while ensuring all other inbound traffic was blocked. The instance was running within the public subnet of my VPC, and the storage settings reflected the default 8 GB general-purpose SSD configuration. To verify everything was working as intended, I tested SSH connectivity using the instance's public IP address and my RSA key pair. Logging into the instance confirmed that the Amazon Linux environment was fully operational and ready for further configurations. This verification ensured that all aspects of the project, including the VPC, subnet, security group, and instance setup, were correctly implemented and functioning seamlessly. :  <br/>
<img src="https://i.imgur.com/IU7ITNg.png" height="80%" width="80%" alt="VPC Steps"/>
<br />
