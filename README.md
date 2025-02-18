# WordPress Hosting on AWS EC2 with RDS (LAMP Stack)

## Overview  
Deployed a **WordPress website** on **Amazon EC2** using the **LAMP stack (Linux, Apache, MySQL, PHP)** with **Amazon RDS** for database management. The setup ensures **scalability, security, and high availability**, utilizing **Elastic Load Balancer (ELB), Auto Scaling, and CloudWatch logging** for monitoring.


## Technologies Used  
- **Amazon EC2** – Hosts the WordPress application.  
- **Amazon RDS (MySQL)** – Managed database for WordPress data.  
- **Apache HTTP Server** – Web server for handling WordPress requests.  
- **PHP** – Server-side scripting for WordPress.  
- **Amazon ELB (Load Balancer)** – Distributes traffic across instances.  
- **Amazon CloudWatch Logs** – Monitors Apache logs for insights.  
- **Auto Scaling Group (ASG)** – Ensures high availability.  

## Features  
✔ **Fully configured WordPress instance with RDS as the database backend.**  
✔ **Scalable architecture with Load Balancer and Auto Scaling.**  
✔ **Centralized logging using CloudWatch for Apache access logs.**  
✔ **Secure MySQL connectivity with restricted access control.**  

---

## Implementation  

### **1. Launched an EC2 Instance and Installed WordPress**
- Deployed an **Amazon Linux 2** EC2 instance.  
- Installed **Apache (httpd) and PHP** for web hosting.  
- Downloaded and extracted **WordPress**.  

### **2. Configured Amazon RDS (MySQL)**
- Created an **RDS MySQL instance** for database management.  
- Configured **security groups** to allow MySQL (3306) connections.  
- Connected to **RDS and created a WordPress database**.  
- Updated **wp-config.php** to point to the **RDS database**.  

### **3. Configured Apache and WordPress**
- Installed **necessary dependencies** (LAMP stack).  
- Moved WordPress files to `/var/www/html/` and restarted Apache.  
- Completed WordPress installation via **browser setup**.  

### **4. Enabled High Availability (HA)**
- Created an **AMI** for the configured EC2 instance.  
- Launched **another EC2 instance** from the AMI.  
- Configured **Target Group (TG)** with a health check at `/`.  
- Set up an **Elastic Load Balancer (ELB)** to distribute traffic.  
- Verified **HA setup** using **ELB DNS name**.  

### **5. Configured Auto Scaling**
- Created a **Launch Template** using the WordPress AMI.  
- Configured **Auto Scaling Group (ASG)** to maintain instance availability.  
- Set scaling policies based on **CPU utilization**.  

### **6. Pushed Apache Logs to CloudWatch**
- Configured CloudWatch Agent to **push Apache logs (`/var/log/httpd/access_log`)**.  
- Created a **CloudWatch log group** for centralized monitoring.  
- Verified logs in the **CloudWatch console**.  

---

## Outcome  
- Successfully deployed a **WordPress website** on AWS with **RDS for database management**.  
- Enabled **high availability** using **Load Balancer and Auto Scaling**.  
- Implemented **Apache access logging to CloudWatch** for monitoring.  
- Optimized performance and **ensured reliability with scalable infrastructure**.  


## Future Enhancements  
- Configure **Amazon S3 for WordPress media storage**.  
- Enable **CloudFront for CDN caching** to improve performance.  
- Automate infrastructure setup with **Terraform**.  

This project demonstrates expertise in **AWS cloud hosting, WordPress deployment, high availability setup, and logging best practices**. 🚀  


