# Laboratory 08 – Cloud Security Engineer

## Mission Overview

This laboratory activity focused on improving cloud server security using the Uncomplicated Firewall (UFW) on Ubuntu. The mission involved deploying an Nginx web application using Docker, checking network accessibility, and configuring firewall rules to protect the server from unauthorized traffic.

## Objectives

- Understand the Principle of Least Privilege (PoLP).
- Identify and reduce a server's attack surface.
- Deploy an Nginx web application using Docker.
- Configure UFW on an Ubuntu server.
- Implement a Default Deny policy for incoming traffic.
- Allow SSH and HTTP application traffic through specific ports.
- Verify firewall rules and application connectivity.
- Document the security configuration using Markdown.

## Commands Executed

### Deploy Nginx Web Application

```bash
docker --version
docker run -d --name secure-web-app -p 8080:80 nginx
docker ps
curl http://localhost:8080
```

### Configure UFW Firewall

```bash
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose
```

### Allow Application Traffic

```bash
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl http://localhost:8080
```

## Skills Learned

- Basic cloud server security
- Docker container deployment
- Linux command-line operations
- Network port management
- UFW firewall configuration
- Default Deny security policy
- SSH and web application access management
- Security auditing and verification
