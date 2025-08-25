# Ansible
Ansible Learning 
# Ansible Learning Project

This repository contains step-by-step examples, notes, and practice files for learning **Ansible** from beginner to advanced level.  

The goal is to understand **what Ansible is, why it is used, how it works, and where it can be applied** in real-world DevOps scenarios.

---

## 📌 What is Ansible?
Ansible is an **open-source configuration management, application deployment, and automation tool**.  
It allows you to manage servers, install software, configure environments, and orchestrate tasks **without manual effort**.

---

## 🚀 Getting Started

### 1. Install Ansible
On Ubuntu/Debian:
```bash
sudo apt update
sudo apt install ansible -y
---

## 🚀 Getting Started

### 1. Install Ansible
On Ubuntu/Debian:
```bash
sudo apt update
sudo apt install ansible -y
sudo yum install epel-release -y
sudo yum install ansible -y
ansible --version
2. Setup SSH Access

Generate SSH keys on the control machine:

ssh-keygen -t rsa -b 2048


Copy public key to target machine:

ssh user@TARGET_SERVER_IP "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys" < ~/.ssh/id_rsa.pub


This allows passwordless login.

3. Configure Inventory File

Edit /etc/ansible/hosts:

[web]
TARGET_SERVER_IP ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/id_rsa

4. Test Connection

Ping all servers in the web group:

ansible -i /etc/ansible/hosts web -m ping

📂 Project Structure
ansible-learning/
│── inventory/        # Hosts and groups
│── playbooks/        # YAML playbooks
│── roles/            # Roles for reusability
│── examples/         # Real-world tasks
│── README.md         # Documentation

✅ Real-World Tasks Covered

Install and configure Nginx/Apache

Manage users and groups

Setup firewall rules

Deploy applications with playbooks

Automate system updates

Orchestrate multi-server deployments

📖 Resources

Ansible Documentation

Ansible GitHub

Ansible Galaxy

🤝 Contributing

Feel free to fork this repo, add your own playbooks, and submit pull requests!
