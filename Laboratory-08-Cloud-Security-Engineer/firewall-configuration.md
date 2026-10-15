# Firewall Configuration

## Overview

This document explains the firewall configuration used in Laboratory 08 – Cloud Security Engineer. The Uncomplicated Firewall (UFW) was used to secure an Ubuntu server by controlling incoming and outgoing network traffic.

## Step 1: Allow SSH Access

```bash
sudo ufw allow ssh
```

This command allows incoming SSH connections through port 22, ensuring that administrators can remotely access and manage the server.

## Step 2: Configure Default Firewall Policies

### Deny Incoming Traffic

```bash
sudo ufw default deny incoming
```

This command blocks incoming network connections unless a specific firewall rule allows them.

### Allow Outgoing Traffic

```bash
sudo ufw default allow outgoing
```

This command allows the server to establish outgoing network connections.

## Step 3: Enable the Firewall

```bash
sudo ufw enable
```

This command activates the UFW firewall and applies the configured security rules.

## Step 4: Check Firewall Status

```bash
sudo ufw status verbose
```

This command displays the current firewall status and its default policies.

The expected configuration includes:

- Firewall Status: Active
- Incoming Traffic: Deny
- Outgoing Traffic: Allow
- SSH Port 22: Allowed

## Step 5: Allow Port 8080

```bash
sudo ufw allow 8080/tcp
```

This command allows incoming TCP traffic through port 8080, which is used by the Nginx web application.

## Step 6: Verify Firewall Rules

```bash
sudo ufw status numbered
```

This command displays the firewall rules in a numbered list.

The expected firewall rules include:

- Port 22/TCP: ALLOW IN
- Port 8080/TCP: ALLOW IN

## Step 7: Verify Web Application Connectivity

```bash
curl http://localhost:8080
```

This command sends an HTTP request to the locally running Nginx web application to verify that it responds successfully.

## Importance of Allowing SSH Before Enabling UFW

If `sudo ufw enable` is executed before `sudo ufw allow ssh`, the firewall may block incoming SSH connections and prevent administrators from remotely accessing the server.
