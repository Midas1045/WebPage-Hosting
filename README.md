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
    * Preparing Website Files
    * Uploading Files to the Virtual Machine
    * Configuring NGINX For Static Hosting
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
* Check the box to run with Azure Spot Discount. This provisions unsused servers, but when needed, your virtual machine can be permanently deleted without     notice.
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
* Skip the Advanced section and proceed to the Tags section, where you can add your name and other relevant details related to the VM creation. Then click     Review/Create
* Validation checks will be carried out to ensure the configurations are correctly set. If passed, you can click Create.
* The deployment is complete, and the virtual machine has been successfully created. Navigate to the VM dashboard to view its details.

 <p align="center"> <img width="800" height="455" alt="Screenshot 2026-02-05 190954" src="https://github.com/user-attachments/assets/e07aae63-f225-4b85-8220-c2548de020c5" />

## Connecting to the Virtual Machine using SSH and verifying connection



     
