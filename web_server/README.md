# Alu System Engineering & DevOps - Web Server

This project focuses on the basics of setting up and configuring an Ubuntu web server. It covers file transfers, software installation (Nginx), and basic server configuration (redirections and custom error pages).

##  Table of Contents
- [Project Overview](#project-overview)
- [Tasks](#tasks)
  - [0. Transfer a file to your server](#0-transfer-a-file-to-your-server)
  - [1. Install nginx web server](#1-install-nginx-web-server)
  - [2. Setup a domain name](#2-setup-a-domain-name)
  - [3. Redirection](#3-redirection)
  - [4. Not found page 404](#4-not-found-page-404)

---

## 🚀 Project Overview
The goal of this project is to automate the deployment of a web server. Instead of manually configuring every server, we use **Bash scripts** to ensure that every new machine is set up identically and efficiently.

---

## 🛠 Tasks

### 0. Transfer a file to your server
A Bash script that transfers a file from a client machine to a remote server's home directory.

**Usage:**
```bash
./0-transfer_file PATH_TO_FILE IP USERNAME PATH_TO_SSH_KEY

