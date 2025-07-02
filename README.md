# 🌐 Ansible Role: Nginx Web Server Setup

This project showcases an Ansible Galaxy-style role to **install, configure, and manage Nginx** on a remote Linux server. It uses best practices such as **handlers**, **variables**, and a modular **role-based structure** 
perfect for learning and demonstrating real-world Ansible automation.
				
---

## 📁 Project Structure
```
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
```

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
```

✅ Verify Ansible Installation:
```bash
ansible --version
```
🗂️ How to Use This Project
🔹 1. Clone the Repository
```bash
git clone https://github.com/Aniruddhakharve/ansible-nginx-role.git
cd ansible-nginx-role
```
🔹 2. Edit Your Inventory File
inventory.ini
```bash
[web]
<your_target_server_ip> ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/id_rsa
```
Replace <your_target_server_ip> and SSH key path as per your setup.

🔹 3. Run the Playbook
```bash
ansible-playbook -i inventory.ini site.yml
```

---
📜 Role Details

webserver/tasks/main.yml

- Installs Nginx
- Copies a custom HTML page
- Notifies handler to restart Nginx

webserver/handlers/main.yml
- Restarts Nginx when notified

webserver/vars/main.yml
```bash
nginx_web_root: /var/www/html
```

webserver/files/index.html
- Contains your custom HTML content served by Nginx.

---

✅ Output Example
After running the playbook, visit:
```bash
http://<your_target_server_ip>
```
You should see:
🚀 Nginx Configured by Ansible Role

---

🧠 Skills Showcased
- ✅ Role-based Ansible automation
- ✅ Use of handlers, vars, defaults, and files
- ✅ Clean, reusable infrastructure code
- ✅ Real-world provisioning with Ansible Galaxy structure

---
🧑‍💻 Author

Aniruddha Kharve

🛠️ MCA Graduate | Linux & DevOps Enthusiast

🔗 GitHub: @Aniruddhakharve

---
⭐ Show Your Support If you found this helpful, please 

⭐ star the repo and share with fellow DevOps learners!





