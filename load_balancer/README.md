# Load Balancer Project

## Description
This project focuses on horizontal scaling by doubling the number of web servers and introducing a load balancer. By distributing traffic across multiple servers, we improve the redundancy and reliability of our infrastructure. 

In this project, I configured two Ubuntu web servers with Nginx and a third server as an HAProxy Load Balancer.

## Concepts Covered
* **Horizontal Scaling:** Increasing capacity by adding more nodes.
* **Load Balancing:** Distributing incoming network traffic across a group of backend servers.
* **HTTP Headers:** Using custom headers to track server responses.
* **Automation:** Using Bash scripts to configure identical server environments.

## Tasks

### 0. Double the number of webservers
**File:** `0-custom_http_response_header`

This script configures a brand new Ubuntu machine to:
* Install and configure Nginx.
* Add a custom HTTP response header: `X-Served-By`.
* The value of this header is the **hostname** of the server (e.g., `[STUDENT_ID]-web-01`).
* This allows us to track which specific server is responding to a request when hidden behind a load balancer.

**Usage:**
```bash
sudo ./0-custom_http_response_header

