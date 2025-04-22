# ansible_nginx_setup
Automate password less EC2 authentication and NGINX installation on AWS using Ansible playbooks.
# 🚀 Ansible Serverless EC2 Setup with NGINX Installation

This project demonstrates how to:
- Set up **passwordless authentication** between an Ansible control node and a target EC2 instance
- Use Ansible to **install and start NGINX** automatically on the target server

This is ideal for DevOps automation practice and cloud configuration management.

---

## 🔧 Technologies Used

- Ansible
- AWS EC2
- Bash
- NGINX
- SSH

---

## 📋 Prerequisites

- Ansible installed on the control node
- Passwordless SSH set up between control and target server ([Setup Guide](docs/passwordless_ssh.md))
- EC2 instance with public IP and security group allowing port 22 & 80

---

## 📁 Usage

1. Clone the repo:
   ```bash
   git clone https://github.com/iam-kvvardhan/ansible-nginx-serverless-setup.git
   cd ansible-nginx-serverless-setup
