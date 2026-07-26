# Proxmox SMART Monitor

Hello everyone! 👋

Although Proxmox includes basic SMART information, I found it somewhat limited and not very user-friendly. I tried several alternatives, but most were either difficult to configure or didn't provide the simple overview I was looking for.

That's why I created **Proxmox SMART Monitor**: a lightweight, visual, and easy-to-use web application that lets you quickly check the SMART health of your Proxmox server's disks.

I hope you find it useful!


## ✨ Features

* 🔍 View SMART information for all disks.
* ❤️ Easy-to-read disk health status.
* 🌐 Simple web interface.
* ⚡ Lightweight and easy to deploy.
* 🐳 Available as a Docker container.

---

# 🚀 Installation

## Prerequisites

* Docker
* Docker Compose

## Docker Compose

Create a `docker-compose.yml` file with the following content:

```yaml
version: '3.8'

services:
  proxmox-smart-monitor:
    image: ghcr.io/mesteve123/proxmox-smart-monitor:v1.1.0
    container_name: proxmox-smart-monitor
    ports:
      - "5000:5000"
    restart: unless-stopped
```

Start the container:

```bash
docker compose up -d
```

Once running, open your browser and go to:

```
http://YOUR_SERVER_IP:5000
```

# 🎨 Dashboard Integration

A custom icon/logo is included for use with self-hosted dashboard applications such as **Homarr**, **Homepage**, **Dashy**, and other homelab dashboards.

You can use the following icon to easily identify **Proxmox SMART Monitor** among your Docker services:

```
https://raw.githubusercontent.com/mesteve123/ProxmoxSMARTMonitor/refs/heads/main/ProxmoxSMARTMonitor.ico
```


---

Thanks for using **Proxmox SMART Monitor**! 🚀
