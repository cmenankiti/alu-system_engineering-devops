# SSH - Web Infrastructure

This project focuses on the fundamentals of remote server management using **Secure Shell (SSH)**. It covers the creation of RSA key pairs, client-side configuration for automated logins, and server-side authorization.

## Background Context
In this project, we interact with a remote Ubuntu 20.04 LTS server hosted in a professional datacenter. Authentication is handled via **Public Key Authentication**, moving away from less secure password-based logins.

## Learning Objectives
By the end of this project, I am able to explain:
* **What a server is**: A physical or virtual machine providing data/services to other computers.
* **Server Locations**: Usually housed in specialized environments called datacenters.
* **What is SSH**: A cryptographic network protocol for operating network services securely over an unsecured network.
* **Key Generation**: How to create an SSH RSA key pair (Private vs. Public).
* **Remote Connection**: How to connect to a host using an identity file.
* **Shebang Best Practices**: The advantage of using `#!/usr/bin/env bash` for better portability across different environments.

## Requirements
* **Environment**: Ubuntu 20.04 LTS.
* **Editors**: `vi`, `vim`, `emacs`.
* **Script Standards**: 
    * All files must end with a new line.
    * All Bash scripts must be executable (`chmod u+x`).
    * First line must be exactly `#!/usr/bin/env bash`.
    * Second line must be a comment explaining the script's purpose.

## Server Information
| Name | Username | IP | State |
| --- | --- | --- | --- |
| 7053-web-01 | ubuntu | 52.91.174.142 | running |

---

## Tasks

| File | Description |
| :--- | :--- |
| [0-use_a_private_key](./0-use_a_private_key) | Bash script that connects to a server using the private key `~/.ssh/school` with the user `ubuntu`. |
| [1-create_ssh_key_pair](./1-create_ssh_key_pair) | Bash script that creates an RSA key pair (4096 bits) named `school` with the passphrase `betty`. |
| [2-ssh_config](./2-ssh_config) | SSH client configuration file configured to use the `school` key and refuse password authentication. |
| **Let me in!** | Task to authorize the evaluator's public key by adding it to the server's `authorized_keys` file. |

## Resources
* [SSH Essentials](https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-t-ssh-servers-clients-and-keys)
* [SSH Config File](https://www.ssh.com/ssh/config/)
* [Public Key Authentication](https://www.ssh.com/ssh/public-key-authentication)

## Author
* **kingm**
