# 🌐 Nginx Multi-Domain Setup Guide

A complete step-by-step guide to setting up **Nginx with multiple domains**, including **MySQL, PHP 8.3, SSL (Certbot), and UFW firewall**.

---

## 📋 Prerequisites

- Linux Server (**Debian/Ubuntu**)
- Root or `sudo` access
- Domain name pointing to your server IP (e.g., `160.x.x.x`)

---

## 🌍 DNS Configuration

Before starting, configure your domain:

1. Go to your domain provider (Namecheap, GoDaddy, etc.)
2. Add the following **A Records**:

| Type | Host | Value      |
|------|------|-----------|
| A    | @    | 160.x.x.x |
| A    | www  | 160.x.x.x |

---

## ⚙️ Step 1: Install Nginx & Firewall

```bash
sudo apt update
sudo apt install nginx -y
sudo ufw allow 'Nginx Full'
