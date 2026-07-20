# Installation Guide

## Lab Requirements

### Hardware

- Minimum 8 GB RAM (16 GB Recommended)
- 50 GB Free Storage
- Intel VT-x / AMD-V Enabled

---

## Operating System

- Kali Linux (Attacker Machine)
- Ubuntu 24.04 LTS (Optional)

---

## Required Software

- Docker
- Burp Suite Community Edition
- Mozilla Firefox
- Git

---

## Step 1: Install Docker

Update your system:

```bash
sudo apt update
sudo apt upgrade -y
```

Install Docker:

```bash
sudo apt install docker.io -y
```

Enable Docker:

```bash
sudo systemctl enable docker
sudo systemctl start docker
```

Verify installation:

```bash
docker --version
```

---

## Step 2: Run OWASP Juice Shop

Pull the Docker image:

```bash
docker pull bkimminich/juice-shop
```

Start the application:

```bash
docker run -d -p 3000:3000 bkimminich/juice-shop
```

Verify the container:

```bash
docker ps
```

Open the application:

```
http://localhost:3000
```

---

## Step 3: Install Burp Suite

Download Burp Suite Community Edition from PortSwigger.

Install it and launch the application.

---

## Step 4: Configure Firefox Proxy

Open:

Settings → Network Settings

Configure:

- Manual Proxy Configuration
- HTTP Proxy: 127.0.0.1
- Port: 8080

Save the settings.

---

## Step 5: Verify Burp Interception

Enable **Intercept is ON** in Burp Suite.

Visit:

```
http://localhost:3000
```

Verify that HTTP requests appear in Burp Suite.

---

## Project Structure

```
web-application-security-lab/
│
├── architecture/
├── notes/
├── payloads/
├── reports/
├── screenshots/
└── setup/
```

---

## Troubleshooting

### Docker container not running

```bash
docker ps
docker start <container-id>
```

### Port 3000 already in use

Stop the existing container or change the mapped port.

### Burp Suite not intercepting traffic

- Check Firefox proxy settings.
- Ensure Burp is listening on port 8080.
- Verify "Intercept is ON".

---

## Disclaimer

This lab is intended for educational purposes only. Perform testing only on systems you own or are explicitly authorized to test.
