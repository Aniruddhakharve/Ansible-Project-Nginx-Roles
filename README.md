# 🌐 Ansible Role: Nginx Web Server Setup

This project showcases an Ansible Galaxy-style role to **install, configure, and manage Nginx** on a remote Linux server. It uses best practices such as **handlers**, **variables**, and a modular **role-based structure** — perfect for learning and demonstrating real-world Ansible automation.
				
---

## 📁 Project Structure
ansible-nginx-role/
├── inventory.ini
├── site.yml
└── webserver/
├── tasks/
│ └── main.yml
├── handlers/
│ └── main.yml
├── files/
│ └── index.html
├── vars/
│ └── main.yml
├── defaults/
│ └── main.yml
└── meta/
└── main.yml


---

## 🚀 What It Does

- Installs **Nginx**
- Deploys a **custom index.html** web page
- Starts and **enables Nginx service**
- Uses **handlers** to restart Nginx on file changes
- Uses **variables** for flexibility and clean code

---

## 🛠️ Prerequisites

- A **Linux control node** (e.g., Ubuntu EC2) with Python 3 and `pip`
- SSH access to the **target machine**
- `git` installed
- `ansible` installed

---

## 📦 Install Ansible

### 🐧 On Ubuntu/Debian:

```bash
sudo apt update
sudo apt install -y python3-pip
pip3 install ansible


