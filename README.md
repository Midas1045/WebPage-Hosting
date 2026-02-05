# Azure Infrastructure Setup: Virtual Machine Provisioning and NGINX Static Web Hosting
This documentation outlines the process of creating and configuring an Azure Virtual Machine and deploying NGINX to host a static website. It covers virtual machine setup, network configuration, web server installation, and deployment of static web content to ensure successful website hosting on Azure.

## Table Of Contents
1. Introduction
2. Prerequisites and Services Used
3. Creation of the Azure Virtual Machine
    * Resource Group Setup
    * Virtual network and Subnet Configuration
    * Network Security Group (NSG) Configuration
    * VM size and Image Selection
    * Authentication Configuration
4. Connecting to the Virtual Machine using SSH and verifying connection
5. NGINX Installation and Configuration
    * Updating the Virtual Machine
    * Installing NGINX
    * Starting and Enabling NGINX
6. Static Website Development
    * Download a Static Website Template
    * Preparing Website Files
    * Uploading Files to the Virtual Machine
    * Configuring NGINX For Static Hosting
    * Update the DNS record to map the IP address of the server
7. Testing and Verification
    * Accessing Website via Public IP
    * Browser Testing
8. Errors and Troubleshooting
9. Conclusion

## Introduction
This project demonstrates the end-to-end setup, including VM provisioning, network and security configuration, web server installation, and deployment of static web content. With this guide, users can gain practical experience in cloud resource management on Azure, understand the basics of web server setup, and ensure that a static website is accessible over the internet in a secure and organized manner.

## Prerequisites and Services Used
* Access to Azure Home Portal
* A valid subscription to create and manage resources
* Availability Zones
* Website Files
* Basic Linux Command Knowledge
* Azure Virtual Machine
* Virtual Network
* Subnets
* Security Groups
* Public IP address
* Storage
* NGINX Web Server
* VSCODE
* Mobaxterm

## Creation of the Azure Virtual Machine
* Navigate to the Azure Portal dashboard and search for Virtual Machines using the Search bar.
* On the Virtual Machines page, click Create.
* On the Basics tab, select the appropriate subscription and enter the name of your resource group.
* Enter the name of your virtual machine and choose its availability region.
* The VM image selected for use is Ubuntu Server 24.04 LTS - x64 Gen2 then choose your ideal architecture.
* Check the box to run with Azure Spot Discount. This provisions unsused servers, but when needed, your virtual machine can be permanently deleted       without notice.
* Select the most ideal VM size for your workload. The size that you choose determines factors such as processing power, memory, and storage capacity.
* On the Administrator section, choose password as the authentication type. Proceed to create a username and password.
* On the Inbound Port Rules section, choose the option for allow selected port and check the boxes for Port 22 for SSH and 80 for HTTP.
* On the Discs Tab, use the default settings provisioned. This include the Operation software type and disk as well as key management.
* For the Networking section, the name of the Virtual Network and Subnet has been automatically filled. Editing them is allowed.
* Request for an IP address which carries a charge and choose how you want your traffic to be routed either through Microsoft or the Internet.
* Select the Basic option for NIC network security group.
* Networking rules for the VM has been set previously so choose the option to delete public IP address and NIC when VM is deleted.
* Leave everything in defaults for the Management Section.
* On the Monitoring Section, check the box to recieve recommended alerts rules. This can be forwarded to you via email. Ensure to add a valid mail.
* Skip the Advanced section and proceed to the Tags section, where you can add your name and other relevant details related to the VM creation. Then     click Review/Create.
* Validation checks will be carried out to ensure the configurations are correctly set. If passed, you can click Create.
* The deployment is complete, and the virtual machine has been successfully created. Navigate to the VM dashboard to view its details.

 <p align="center"> <img width="800" height="455" alt="Screenshot 2026-02-05 190954" src="https://github.com/user-attachments/assets/e07aae63-f225-4b85-8220-c2548de020c5" />

## Connecting to the Virtual Machine using SSH and verifying connection
This covers how to securely connect to the virtual machine using SSH. An SSH client is used to establish a remote connection to the VM, allowing direct access to the server for configuration, management, and verification tasks.
* To connect to the virtual machine, MobaXterm was used as the SSH client.
* The public IP address of the VM and the configured username were entered into MobaXterm to initiate the SSH connection.
* Upon successful authentication, access to the VM’s terminal was established.
* Connection was verified by executing basic commands on the VM, confirming that the instance was reachable and responding as expected. These commands   include pwd, id, id root, whoami, who etc. 

<p align="center"> <img width="800" height="455" alt="Screenshot 2026-02-05 192912" src="https://github.com/user-attachments/assets/2127da89-0e84-4445-8b73-e2b4b2a283bd" />

## NGINX Installation and Configuration
This section covers the steps used in installing and configuring NGINX on the virtual machine. NGINX is used as the web server to serve static web content, and proper configuration ensures that the website is accessible and runs efficiently.
* On the initiated session on Mobaxtern, Use the command "sudo apt update". This updates the VM package list to ensure the latest software is            available for installation.
* If there are items to be upgraded, use this command "apt list --upgradable" to list them.
* The next step is to upgrade these items using the command "sudo apt upgrade". It ensures that all installed packages are updated to their latest       versions.
* After upgrading, install NGINX using the command "sudo apt install nginx -y". This command installs the NGINX web server along with all required       dependencies.
* Use the command "sudo systemctl status nginx " to check if NGINX is operational.
* The next step is to locate the web folder. Use the "cd /var" command.
* On the var folder, use the "ls" command to show the list of files in this folder. (backups, cache, crash, lib, local, lock, log, mail, opt, run,       snap, spool, tmp, www).
* Use the "cd www" command to access the 'www' folder. In the 'www' folder, use the command 'll' or 'ls -l' to list files present in a long format.
* Navigate to the html file using the command "cd html". Then use the "ls" command to list the files in the html folder. This contains a small web       content file- index.nginx-debian.html. 
* To display the contents of the index.nginx-debian.html file, we use the "cat" command. "cat index.nginx-debian.html". If NGINX web server is working   well, the default NGINX welcome page should be displayed when you navigate to your VM’s public IP address in a web browser. This shows that your       server is running and ready to serve web content.
* To edit the text on NGINX welcome page, use the command "sudo nano index.nginx-debian.html to switch to notepad mode where you can make adjustments    and save using CTRL+S. Then refresh your page.

<p align="center"> <img width="800" height="419" alt="Screenshot 2026-02-05 200433" src="https://github.com/user-attachments/assets/3dec24b5-87a9-44a5-95d3-70c2f1f2eda2" />

## Static Website Development
This section covers the creation and deployment of a static website on the NGINX web server. A static website consists of fixed content such as HTML, CSS, images, and JavaScript files that do not change dynamically. By deploying static web pages, users can host simple, fast, and secure websites ideal for portfolios or informational pages.
* To download a static website template, visit themewagon.com and select the template that best fits your needs.
* After downloading the template, extract the contents of the zipped file to access the website files.
* 

* 



