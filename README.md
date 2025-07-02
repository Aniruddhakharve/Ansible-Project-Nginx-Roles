# 🌐 Ansible Role: Nginx Web Server Setup

This project showcases an Ansible Galaxy-style role to **install, configure, and manage Nginx** on a remote Linux server. It uses best practices such as handlers, variables, and modular role-based structure — perfect for learning and demonstrating real-world Ansible automation.

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

1. **Linux control node** (like Ubuntu EC2) with Python 3 and `pip`
2. SSH access to the **target machine**
3. Git installed
4. Python + Ansible installed (see below)

---

## 📦 Install Ansible

### 🐍 For Ubuntu/Debian:
```bash
sudo apt update
sudo apt install -y python3-pip
pip3 install ansible

🧪 Verify Installation:

ansible --version

🗂️ How to Use This Project

🔹 1. Clone the Repository
git clone https://github.com/Aniruddhakharve/ansible-nginx-role.git
cd ansible-nginx-role

🔹 2. Edit Your Inventory File
inventory.ini

[web]
<your_target_server_ip> ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/id_rsa

🔹 3. Run the Playbook
ansible-playbook -i inventory.ini site.yml

📜 Role Details
webserver/tasks/main.yml
Installs Nginx

Copies a custom HTML page

Notifies handler to restart service if file changes

webserver/handlers/main.yml
Restarts Nginx if notified

webserver/vars/main.yml
nginx_web_root: /var/www/html

webserver/files/index.html
Your custom web content (HTML).

✅ Output Example
After running the playbook, visit:
http://<your_target_server_ip>
You’ll see your custom web page:
"🚀 Nginx Configured by Ansible Role"

🧠 Skills Showcased
- Role-based Ansible design
- Use of handlers, vars, and defaults
- Modular and reusable infrastructure code
- Real-world provisioning and automation

🧑‍💻 Author
Aniruddha Kharve
🛠️ MCA Graduate | Linux & DevOps Enthusiast
🔗 GitHub: @Aniruddhakharve


⭐ Show Your Support
If you found this helpful, leave a ⭐ on the repo and share with fellow DevOps learners!


