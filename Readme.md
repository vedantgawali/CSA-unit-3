# AWS EC2 Web Application

## Project Overview
This project demonstrates how to deploy a simple HTML web application on an Amazon EC2 Linux instance using the Nginx web server.

## Technologies Used
- Amazon Web Services (AWS)
- Amazon EC2
- Linux
- Nginx
- HTML and CSS

## Features
- Cloud-based web hosting
- Custom HTML web page
- HTTP access through port 80
- SSH administration through port 22
- Security group configuration

## Deployment Steps
1. Launch a Linux EC2 instance.
2. Create a security group allowing SSH from the administrator's IP and HTTP on port 80.
3. Connect to the instance.
4. Install and start Nginx.
5. Place the custom `index.html` file in `/var/www/html/`.
6. Verify the Nginx configuration and service.
7. Open the instance's public IPv4 address in a browser.

## Commands

Update packages:

```bash
sudo apt update
```

Install Nginx:

```bash
sudo apt install nginx -y
```

Start Nginx:

```bash
sudo systemctl enable --now nginx
```

Test Nginx configuration:

```bash
sudo nginx -t
```

## Security
- SSH (port 22) is restricted to the administrator's IP address.
- HTTP (port 80) is enabled for public website access.
- Private SSH keys must never be uploaded to this repository.

## Project Result
The custom HTML page is served by Nginx on an Amazon EC2 instance. See the screenshots folder for deployment evidence.

## Disclaimer
This is an educational cloud security project. HTTP is used for demonstration; HTTPS should be configured for production deployments.
