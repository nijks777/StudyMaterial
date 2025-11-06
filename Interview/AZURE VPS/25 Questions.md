Easy (Beginner) – 5 Questions

What is a VPS, and how is it different from shared hosting?

Which command is used to update packages in Ubuntu?
sudo apt update && sudo apt upgrade

What is SSH and why is it used?

How do you check the status of a running service in Ubuntu?
Example: systemctl status nginx

What is the purpose of a firewall? Name one commonly used firewall in Ubuntu.
Example: UFW

⚡ Medium (Core + Scenario Based) – 15 Questions

In Hostinger Ubuntu VPS, how would you secure SSH to prevent brute-force attacks?
(E.g., change port, disable password login, enable key-based auth, fail2ban)

You deployed a web application on NGINX but it shows 502 Bad Gateway. What could be the common causes?

Explain the difference between Nginx and Apache and when you would choose one over the other.

How do you set up a domain on Hostinger VPS using Cloudflare DNS?
(Steps: Nameservers → DNS A record → SSL mode → proxy)

Scenario:
You uploaded your site to /var/www/html, but when visiting the domain you still see “Hostinger Default Page”.
What steps would you take to fix it?

How do you configure a Reverse Proxy using NGINX for a Node.js application running on port 3000?

Explain how to generate and install SSL certificates using Let's Encrypt & Certbot.

What is a Service Unit in systemd and how do you create a persistent service for a Flask/Node.js app?

In Azure, what is the difference between App Service and Virtual Machine hosting?

Scenario:
You deployed an app on Azure App Service but it’s failing due to dependency versions.
How do you troubleshoot and fix it?

Explain Azure Virtual Network (VNet) and how it helps in network segmentation.

What is Azure Load Balancer vs Azure Application Gateway? When to use each?

How do you implement CI/CD in Azure DevOps for deploying code to Hostinger VPS or Azure VM?

You have a Python/Node app that crashes after server reboot. How do you ensure it starts automatically?
(systemd service or pm2)

Scenario:
You need to scale your web backend due to traffic spikes.
How would your approach differ between Hostinger VPS and Azure-based infrastructure?

🔥 Difficult (Advanced & Architecture) – 5 Questions

How do you set up Zero-Downtime Deployment for a Node.js or Flask app on an Ubuntu VPS?
(Load balancer, rolling restart, blue-green deployment, PM2 cluster mode)

Explain the steps to configure NGINX + Cloudflare + Fail2ban + UFW to prevent DDoS and brute-force attacks.

How would you migrate a production application from a Hostinger VPS to Azure VM or Azure App Service with minimal downtime?
(DNS TTL reduction, parallel environment, blue/green switch-over)

Scenario:
Your application needs to store files, logs, and backups reliably. Compare using:

Local VPS Disk

Azure Blob Storage

Azure Files
When would you choose each?

Design a secure multi-tier architecture in Azure:

Frontend Web App

Backend API

Database

Load Balancer

Firewalls & VNet
Explain the network flow and access controls.