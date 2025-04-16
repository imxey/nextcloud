# ☁️ Nextcloud with Docker - Setup Guide

Welcome to your personal **Nextcloud** setup powered by Docker! 🚀  
This guide will help you install and run Nextcloud using Docker in just a few steps.

---

## 🔧 Installation Guide

### 🐳 Step 1: Install Docker (Linux)

```bash
# Update package index & install required dependencies
sudo apt-get update
sudo apt-get install ca-certificates curl

# Add Docker's official GPG key
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Set up the Docker repository
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Install Docker Engine and related tools
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Final step to make sure Docker is installed
docker -v

```
### 🐳 Step 2: Clone Repo 

```bash
sudo apt install git
git clone https://github.com/imxey/nextcloud
cd nextcloud
```
### 🐳 Step 3: Run Docker 

```bash
sudo docker compose up -d
or
sudo docker-compose up -d
