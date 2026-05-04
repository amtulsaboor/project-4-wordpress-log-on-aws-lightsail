# Deploying a WordPress on AWS Lightsail

Deploying a WordPress blog using Amazon Web Services Lightsail with static IP, SSL configuration, and basic security optimizations.

---

## Project Overview

This project demonstrates how to deploy a WordPress website using **AWS Lightsail**, a simplified cloud hosting service offered by Amazon Web Services.

Using Lightsail’s pre-configured WordPress blueprint, I launched a server, configured networking, retrieved admin credentials, enabled HTTPS, and secured the website.

---

## Architecture

```plaintext
User → Browser → AWS Lightsail Instance → WordPress Application
                         |
                         → Static IP
                         → SSL Certificate
                         → Custom Domain (Optional)
```

---

## Technologies Used

* Amazon Web Services AWS Lightsail
* WordPress WordPress
* Bitnami Stack
* SSH
* SSL/TLS
* DNS Configuration

---

## Steps Performed

### 1. Create Lightsail Instance

* Logged into AWS Console
* Opened Lightsail
* Clicked **Create Instance**
<img width="1710" height="1107" alt="Screenshot 2026-05-05 at 12 39 59 AM" src="https://github.com/user-attachments/assets/3daeb221-ca11-4e17-8642-b3482048f991" />

---

### 2. Select Region

* Chose the nearest AWS region for better latency

---

### 3. Choose WordPress Blueprint

* Selected:

  * Apps + OS
  * WordPress
<img width="1710" height="1107" alt="Screenshot 2026-05-05 at 1 45 37 AM" src="https://github.com/user-attachments/assets/8bc521f1-c824-485f-8b25-73b1f85372cb" />

---

### 4. Select Pricing Plan

* Chose the basic plan suitable for small websites

---

### 5. Launch Instance

* Named instance:

```bash id="0czvnl"
wordpress-blog-project
```

* Created instance

---

## Access Website

Copy the public IP and open:

```id="xih5mq"
http://your-public-ip
```
<img width="1710" height="1107" alt="Screenshot 2026-05-05 at 12 43 53 AM" src="https://github.com/user-attachments/assets/131339ca-9adb-4c4a-9846-1470bfa942f9" />

---

## Retrieve WordPress Password

Connect via SSH and run:

```bash id="0wyy6f"
cat bitnami_application_password
```
<img width="1710" height="1107" alt="Screenshot 2026-05-05 at 1 23 13 AM" src="https://github.com/user-attachments/assets/cb00dc49-c7b0-460c-b52a-629c27203300" />

---

## Login to WordPress Admin

```id="8w0s7j"
http://your-public-ip/wp-admin
```
<img width="1710" height="1107" alt="Screenshot 2026-05-05 at 1 00 40 AM" src="https://github.com/user-attachments/assets/b295c442-5fc4-4653-aaaf-b18c48696eb7" />

---

## Configure Static IP

* Navigate to Networking
* Create Static IP
* Attach to instance

---

## Enable SSL

Run:

```bash id="x9j60e"
sudo /opt/bitnami/bncert-tool
```

This enables HTTPS for secure communication.

---

## Optional Domain Setup

* Purchase domain
* Update A record
* Point domain to Lightsail static IP

---

## Security Improvements

* Updated WordPress plugins
* Installed security plugins
* Enabled backups

---

## Backup Strategy

Used Lightsail snapshots for backup and disaster recovery.

---

## Project Outcome

✅ Successfully deployed WordPress on AWS Lightsail
✅ Configured server networking
✅ Enabled HTTPS security
✅ Learned cloud deployment basics

---

## Repository Structure

```plaintext
├── README.md
├── screenshots/
└── documentation/
```

---

## Future Improvements

* CI/CD deployment pipeline
* CloudFront integration
* Database optimization
* Monitoring setup

---

## Author

**Amtul Saboor**
DevOps & Cloud Engineer 


