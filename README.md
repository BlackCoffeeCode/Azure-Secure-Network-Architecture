# Azure Secure Network Architecture

A comprehensive guide to building a secure network infrastructure on Microsoft Azure with virtual networks, bastion hosts, firewalls, and web services.

## 📋 Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Architecture](#architecture)
- [Steps](#steps)
- [Quick Start](#quick-start)
- [Support](#support)

## 📚 Overview

This project provides a step-by-step guide to create a production-ready Azure network infrastructure with the following components:

- **Azure Virtual Network (VNet)**: Isolated network environment for your resources
- **Bastion Host**: Secure, browser-based RDP/SSH access without exposing VMs to the internet
- **Azure Firewall**: Centralized protection for inbound and outbound traffic
- **Web Server (Nginx)**: Running on an Azure Virtual Machine
- **Network Security**: DNAT rules and firewall policies for secure communication

## ✅ Prerequisites

Before you begin, ensure you have:

- An active Azure subscription
- Azure Portal access
- Basic understanding of networking concepts
- Azure CLI or PowerShell (optional, for automation)
- A modern web browser

## 🏗️ Architecture

```
┌─────────────────────────────────────────┐
│        Azure Virtual Network (VNet)     │
├─────────────────────────────────────────┤
│                                         │
│  ┌──────────────────────────────────┐  │
│  │   Azure Bastion                  │  │
│  │   (Secure RDP/SSH Access)        │  │
│  └──────────────────────────────────┘  │
│                                         │
│  ┌──────────────────────────────────┐  │
│  │   Virtual Machine                │  │
│  │   ├─ Nginx Web Server            │  │
│  │   └─ HTML Content                │  │
│  └──────────────────────────────────┘  │
│                                         │
└─────────────────────────────────────────┘
              ↓
┌─────────────────────────────────────────┐
│   Azure Firewall (DNAT Rules)           │
│   ├─ Inbound Traffic Management         │
│   └─ Outbound Security Policies         │
└─────────────────────────────────────────┘
```

## 🚀 Steps

### STEP1: Create Virtual Network (VNet)

[📺 View the interactive tutorial on Scribe](https://scribehow.com/embed/Creating_an_Azure_Virtual_Network_with_Bastion_and_Firewall__EfzvlzeyQlWKsSpJca8a_w)

This step covers creating an Azure Virtual Network with Bastion and Firewall components. For more details, see [VNet.md](VNet.md)

### STEP2: Create a Virtual Machine inside the VNet

[📺 View the interactive tutorial on Scribe](https://scribehow.com/embed/Step_2_Create_A_Virtual_Machine_In_Azure__2QE7CmsjSZmivpwankbVtA)

This step covers creating a virtual machine within your Azure Virtual Network. For more details, see [Virtual_Machine.md](Virtual_Machine.md)

### STEP3: Connect Bastion

[📺 View the interactive tutorial on Scribe](https://scribehow.com/embed/How_To_Connect_To_Azure_Virtual_Machines_Using_Bastion__BPImFZFrRuaM6R7yCqYyvQ)

This step covers connecting to your Azure Virtual Machines using Azure Bastion for secure access. For more details, see [Connect_Bastion.md](Connect_Bastion.md)

### STEP4: Install Nginx in Machine

[📺 View the interactive tutorial on Scribe](https://scribehow.com/embed/Azure_Workflow__-HdhrMdgTU-6Z87EwESTeA)

This step covers installing and configuring nginx on your Azure Virtual Machine. For more details, see [Install_Nginx.md](Install_Nginx.md)

### STEP5: Create a HTML Page into Nginx and Restart Nginx

[📺 View the interactive tutorial on Scribe](https://scribehow.com/embed/Azure_Workflow__wnc-Y813RXaq-j1S7Li9vw)

This step covers creating an HTML page and deploying it to nginx, then restarting the nginx service. For more details, see [Create_HTML_Nginx.md](Create_HTML_Nginx.md)

### STEP6: Configure the Firewall

[📺 View the interactive tutorial on Scribe](https://scribehow.com/embed/Configuring_A_DNAT_Rule_For_Azure_Firewall__v9mxQ5nCRhy5Wqa2z24jnA)

This step covers configuring Azure Firewall with DNAT rules to manage traffic to your resources. For more details, see [Configure_Firewall.md](Configure_Firewall.md)

## ⚡ Quick Start

To get started quickly:

1. **STEP1**: Create a Virtual Network with Bastion and Firewall components
2. **STEP2**: Deploy a Virtual Machine within your VNet
3. **STEP3**: Connect to your VM securely using Bastion
4. **STEP4**: Install nginx web server on your VM
5. **STEP5**: Create and deploy an HTML page to nginx
6. **STEP6**: Configure firewall rules to manage incoming traffic

Each step includes an interactive tutorial video to guide you through the process.

## 🔒 Security Best Practices

- Use Azure Bastion instead of exposing VMs to the public internet
- Configure Azure Firewall to control inbound and outbound traffic
- Keep your network segmentation using subnets and Network Security Groups (NSGs)
- Regularly review and update firewall rules
- Use HTTPS for web traffic whenever possible
- Enable logging and monitoring for security events

## 📖 Learning Resources

- [Azure Virtual Networks Documentation](https://learn.microsoft.com/en-us/azure/virtual-network/)
- [Azure Bastion Documentation](https://learn.microsoft.com/en-us/azure/bastion/)
- [Azure Firewall Documentation](https://learn.microsoft.com/en-us/azure/firewall/)
- [Nginx Official Documentation](https://nginx.org/en/docs/)

## 💬 Support

For questions or issues:

1. Check the individual step documentation files (*.md files)
2. Review the Azure documentation links provided above
3. Consult the Scribe tutorial videos embedded in each step
4. Visit [Azure Support](https://azure.microsoft.com/en-us/support/)

## 📄 License

This project is provided as-is for educational purposes.

---

**Last Updated**: August 2026
**Repository**: [Azure-Secure-Network-Architecture](https://github.com/BlackCoffeeCode/Azure-Secure-Network-Architecture)
