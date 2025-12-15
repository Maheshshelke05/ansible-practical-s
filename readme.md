# Ansible – Introduction & Purpose

## What is Ansible?

Ansible is an **open-source automation tool** used to automate **configuration management, application deployment, and server setup**.  
It is **agentless**, meaning no agent is required on managed nodes, and it works using **SSH and YAML-based playbooks**.

Ansible helps system administrators and DevOps engineers manage infrastructure in a simple, reliable, and repeatable way.

---

## Purpose of Ansible in a DevOps Career

In DevOps, Ansible is widely used to:

- Automate repetitive server and operational tasks  
- Maintain consistency across multiple servers  
- Reduce manual configuration errors  
- Speed up deployments and day-to-day operations  

Ansible enables DevOps engineers to manage infrastructure **efficiently, reliably, and at scale**, making it a critical tool in modern DevOps workflows.

---

## Key Benefits

- Agentless architecture  
- Easy to learn and human-readable (YAML)  
- Scales from single server to large infrastructure  
- Integrates well with CI/CD tools like Jenkins, GitHub, and Terraform

---

## Conclusion

Ansible is a core DevOps tool that simplifies automation, improves reliability, and increases operational efficiency across environments.
---

## How to install Ansible in aws ec2 instance
1. **Connect to your EC2 instance** via SSH:
   ```bash
   ssh -i your-key.pem ec2-user@your-ec2-public-dns
   ```
2. **Update the package index**:
   ```bash
   sudo yum update -y
   ```
3. **Install Ansible**:
   ```bash
   sudo yum install ansible2 -y
   ```
4. **Verify the installation**:
   ```bash
   ansible --version
   ```
5. **hostname**
   ```bash
   sudo hostnamectl set-hostname ansible-server
   sudo yum update -y
   ```
---

# My First Ansible Project – Ping Test

## Project Overview
This is my **first Ansible project**, created to understand the basics of Ansible automation and connectivity testing.
link:https://github.com/Maheshshelke05/ansible-practical-s/blob/90f5fd7e397798a725a7c98594afea7011d3ed6e/ping.yml

The project uses an Ansible playbook to **check whether target servers are reachable** using the Ansible ping module.

---

## What This Project Does
- Verifies connectivity between Ansible control node and target host(s)
- Confirms SSH access and Ansible configuration
- Ensures Ansible is working correctly before running real automation tasks

---

## How It Works
1. Ansible runs the playbook from the **control node**
2. The playbook targets the specified host (localhost or remote server)
3. Ansible uses **SSH** to connect to the host
4. The `ping` module checks communication
5. If successful, Ansible returns **“pong”**

---

## Technologies Used
- Ansible
- YAML
- SSH
- Linux

---

# Ansible Second Project – Create File / Folder Automation

## Project Overview
This is my **second Ansible project**, created to understand how Ansible can be used to **create files or directories automatically** on a server.

This project demonstrates basic **configuration management** using Ansible.

link:https://github.com/Maheshshelke05/ansible-practical-s/blob/90f5fd7e397798a725a7c98594afea7011d3ed6e/create_file.yml

---

## What This Project Does
- Creates a file or directory on the target system
- Sets permissions automatically
- Removes the need for manual Linux commands like `mkdir` or `touch`

---

## How It Works
1. Ansible runs the playbook from the control node
2. The playbook targets `localhost` (or any configured host)
3. Ansible connects using **SSH**
4. The `ansible.builtin.file` module is executed
5. The specified file or folder is created with defined permissions

---

## Technologies Used
- Ansible
- YAML
- Linux
- SSH

---

# Ansible Third Project – Directory Creation Automation

## Project Overview
This is my **third Ansible project**, created to understand how Ansible automates **directory creation and permission management** on Linux systems.

The project focuses on using the Ansible `file` module for basic infrastructure automation.

link:https://github.com/Maheshshelke05/ansible-practical-s/blob/90f5fd7e397798a725a7c98594afea7011d3ed6e/create_folder.yml

---

## What This Project Does
- Creates a directory at a specified path
- Sets directory permissions automatically
- Eliminates manual Linux commands like `mkdir` and `chmod`

---

## How It Works
1. Ansible playbook runs from the control node
2. Target host is defined as `localhost` (or remote servers)
3. Ansible connects using **SSH**
4. The `ansible.builtin.file` module is executed
5. Directory is created with defined permissions

---

## Technologies Used
- Ansible
- YAML
- Linux
- SSH
---

# Ansible Fourth Project – HTTPD Installation Automation

## Project Overview
This is my **fourth Ansible project**, focused on automating the **installation and management of the Apache HTTP (httpd) web server** using Ansible.

This project demonstrates how Ansible is used in real-world scenarios to install and manage services.

link:https://github.com/Maheshshelke05/ansible-practical-s/blob/90f5fd7e397798a725a7c98594afea7011d3ed6e/http_install.yml

---

## What This Project Does
- Installs the Apache HTTPD package
- Starts the HTTPD service
- Ensures the service runs automatically on system boot

---

## How It Works
1. Ansible playbook is executed from the control node
2. Target host is defined (localhost or remote servers)
3. Ansible connects via **SSH**
4. Package is installed using the package manager
5. HTTPD service is started and enabled

---

## Technologies Used
- Ansible
- YAML
- Linux
- Apache HTTPD
- SSH
---

# Ansible Fifth Project – Nginx Installation Automation

## Project Overview
This is my **fifth Ansible project**, created to automate the **installation and management of the Nginx web server** using Ansible.

This project reflects a common real-world DevOps task: preparing servers to host web applications.

link:https://github.com/Maheshshelke05/ansible-practical-s/blob/90f5fd7e397798a725a7c98594afea7011d3ed6e/nginx_install.yml

---

## What This Project Does
- Installs the Nginx package
- Starts the Nginx service
- Enables Nginx to start automatically on system reboot

---

## How It Works
1. Ansible playbook runs from the control node
2. Target host is specified (localhost or remote servers)
3. Ansible connects using **SSH**
4. Nginx package is installed via the system package manager
5. Nginx service is started and enabled

---

## Technologies Used
- Ansible
- YAML
- Linux
- Nginx
- SSH
---

# Ansible Sixth Project – Tree Package Installation

## Project Overview
This is my **sixth Ansible project**, created to automate the **installation of the `tree` package** using Ansible.

This project demonstrates basic **package management automation** with Ansible.

link:- https://github.com/Maheshshelke05/ansible-practical-s/blob/90f5fd7e397798a725a7c98594afea7011d3ed6e/tree_install.yml

---

## What This Project Does
- Installs the `tree` package on the target system
- Verifies package installation using Ansible automation
- Eliminates manual package installation commands

---

## How It Works
1. Ansible playbook is executed from the control node
2. Target host is defined (localhost or remote servers)
3. Ansible connects to the host using **SSH**
4. Package is installed via the system package manager
5. Installation completes successfully

---

## Technologies Used
- Ansible
- YAML
- Linux
- SSH

---

# Ansible Seventh Project – LAMP Stack Automation

## Project Overview
This is my **seventh Ansible project**, focused on automating the **LAMP stack (Linux, Apache, MySQL, PHP)** installation using Ansible.

This project demonstrates a real-world DevOps use case where Ansible is used to prepare a complete web application environment.

link:https://github.com/Maheshshelke05/ansible-practical-s/blob/90f5fd7e397798a725a7c98594afea7011d3ed6e/lamp.yml

---

## What This Project Does
- Installs Apache (httpd) web server
- Installs MySQL database server
- Installs PHP and required PHP modules
- Starts and enables required services

---

## How It Works
1. Ansible playbook runs from the control node
2. Target host is defined (localhost or remote servers)
3. Ansible connects using **SSH**
4. Required packages are installed automatically
5. Apache and MySQL services are started and enabled

---

## Technologies Used
- Ansible
- YAML
- Linux
- Apache HTTPD
- MySQL
- PHP
- SSH

---
