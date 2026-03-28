# Firewall - Server Security

This project focuses on securing **web-01** using **UFW** (Uncomplicated Firewall). The goal is to implement a "Default Deny" policy to reduce the attack surface of the server while allowing essential traffic for web services and administrative access.

## Concepts Covered
* **UFW (Uncomplicated Firewall):** A user-friendly interface for managing iptables.
* **Inbound vs. Outbound Traffic:** Understanding the direction of network packets.
* **Port Management:** Whitelisting specific TCP ports (22, 80, 443).
* **Network Debugging:** Using `telnet` to verify open and closed sockets.

---

## Tasks

### 0. Block all incoming traffic but...
This task involves setting up a firewall on **web-01** that blocks all incoming traffic by default but allows the three most critical ports for a web server.

* **File:** `0-block_all_incoming_traffic_but`
* **Rules Applied:**
    * **Default Inbound:** Deny
    * **Default Outbound:** Allow
    * **Port 22 (SSH):** Allow (For remote management)
    * **Port 80 (HTTP):** Allow (For standard web traffic)
    * **Port 443 (HTTPS):** Allow (For secure web traffic)

---

## Usage and Setup

### 1. Running the script
To apply these rules to your server, run the script with root privileges:

```bash
chmod +x 0-block_all_incoming_traffic_but
sudo ./0-block_all_incoming_traffic_but
