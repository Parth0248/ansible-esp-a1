# Ansible Web Server Deployment

**Enterprise Software Platforms - Assignment 1**

This project demonstrates automated deployment of web servers on Google Cloud Platform using Ansible automation.

## 🚀 Overview

- **Objective**: Deploy web servers on two VMs displaying custom messages
- **Platform**: Google Cloud Platform (GCP)
- **Automation**: Ansible playbooks
- **Web Server**: Python HTTP server on port 8080

## 📁 Project Structure

```
ansible-webserver-project/
├── README.md
├── ansible.cfg                    # Ansible configuration
├── inventory/
│   └── hosts                      # VM inventory file
├── playbooks/
│   ├── deploy-webserver.yml       # Deployment playbook
│   └── undeploy-webserver.yml     # Cleanup playbook
└── files/
    ├── index_vm1.html             # VM1 web page
    └── index_vm2.html             # VM2 web page
```

## 🛠️ Setup Requirements

- Google Cloud Platform account with compute credits
- 2 VMs created (`vm1-webserver`, `vm2-webserver`)
- Firewall rule allowing port 8080
- Google Cloud Shell (Ansible pre-configured)

## ⚡ Quick Start

### 1. Test Connectivity
```bash
ansible webservers -m ping
```

### 2. Deploy Web Servers
```bash
ansible-playbook playbooks/deploy-webserver-embedded.yml
```

### 3. Access Websites
- **VM1**: `http://VM1_EXTERNAL_IP:8080` → "Hello World from SJSU-1"
- **VM2**: `http://VM2_EXTERNAL_IP:8080` → "Hello World from SJSU-2"

### 4. Cleanup (when done)
```bash
ansible-playbook playbooks/undeploy-webserver.yml
```

## 📋 What Gets Deployed

- **Python HTTP Server**: Lightweight web server on port 8080
- **Custom HTML Pages**: Styled pages with assignment-specific messages
- **System Service**: Auto-starting systemd service
- **Directory Structure**: Organized web content in `/opt/webserver/`

## 🔧 Key Features

- ✅ **Idempotent**: Safe to run multiple times
- ✅ **Automated**: Complete hands-off deployment
- ✅ **Clean Removal**: Complete cleanup with undeploy
- ✅ **Professional**: Styled HTML with responsive design
- ✅ **Reliable**: Error handling and service management

## 🎯 Assignment Deliverables

- [x] Two VMs with web servers on port 8080
- [x] Custom messages: "Hello World from SJSU-1" and "SJSU-2"
- [x] Deploy and undeploy playbooks
- [x] Complete documentation and screenshots
- [x] GitHub repository with all code

## 🛡️ Security

- SSH key-based authentication
- Minimal user permissions (`nobody:nogroup`)
- Firewall rules for specific ports only
- No hardcoded credentials

## 📸 Demo

The deployment creates professional-looking web pages with:
- Responsive design
- Color-coded themes (blue for VM1, orange for VM2)
- Assignment branding
- Success confirmation messages

## 🎓 Learning Outcomes

- Infrastructure as Code (IaC) principles
- Ansible automation and playbook development
- Cloud infrastructure management
- System administration and service management
- DevOps best practices

---

**Author**: Parth Maradia 
**Course**: Enterprise Software Platforms  
**Institution**: San José State University
