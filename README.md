🌐 Ansible Role: Nginx Web Server Setup
This project showcases an Ansible Galaxy-style role to install, configure, and manage Nginx on a remote Linux server. It uses best practices such as handlers, variables, and modular role-based structure — perfect for learning and demonstrating real-world Ansible automation.

📁 Project Structure
ansible-nginx-role/
├── inventory.ini
├── site.yml
└── webserver/
  ├── tasks/
  │  └── main.yml
  ├── handlers/
  │  └── main.yml
  ├── files/
  │  └── index.html
  ├── vars/
  │  └── main.yml
  ├── defaults/
  │  └── main.yml
  └── meta/
    └── main.yml

🚀 What It Does
Installs Nginx

Deploys a custom index.html web page

Starts and enables Nginx service

Uses handlers to restart Nginx on file changes

Uses variables for flexibility and clean code

🛠️ Prerequisites
A Linux control node (e.g., Ubuntu EC2) with Python 3 and pip installed

SSH access to the target machine

Git installed

Ansible installed

📦 Install Ansible (Ubuntu/Debian)
sudo apt update
sudo apt install -y python3-pip
pip3 install ansible

To verify Ansible installation:
ansible --version

🗂️ How to Use This Project
Clone the Repository

git clone https://github.com/Aniruddhakharve/ansible-nginx-role.git
cd ansible-nginx-role

Edit Your Inventory File

Open the file named inventory.ini and add your server details:

[web]
<your_target_server_ip> ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/id_rsa

Replace <your_target_server_ip> with your actual server IP.

Run the Playbook

ansible-playbook -i inventory.ini site.yml

If your server requires sudo, you can also run:

ansible-playbook -i inventory.ini site.yml --ask-become-pass

📜 Role Details
webserver/tasks/main.yml

Installs Nginx

Copies a custom HTML page

Notifies handler to restart Nginx

webserver/handlers/main.yml

Restarts Nginx when notified

webserver/vars/main.yml
Contains:
nginx_web_root: /var/www/html

webserver/files/index.html
Contains your custom HTML content served by Nginx.

✅ Output Example
After running the playbook, open your browser and visit:
http://<your_target_server_ip>

You should see the custom message:
"🚀 Nginx Configured by Ansible Role"

🧠 Skills Showcased
Role-based Ansible automation

Use of handlers, vars, defaults, and files

Clean, reusable infrastructure code

Real-world provisioning with Ansible Galaxy structure

🧑‍💻 Author
Aniruddha Kharve
MCA Graduate | Linux & DevOps Enthusiast
GitHub: https://github.com/Aniruddhakharve

⭐ Show Your Support
If you found this helpful, please ⭐ star the repo and share it with your fellow DevOps learners!

