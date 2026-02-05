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
  1. Resource Group Setup
     
