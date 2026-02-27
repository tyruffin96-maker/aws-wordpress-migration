🚀 AWS Legacy Application Migration Project
📌 Overview
This project demonstrates the migration of a legacy web application to AWS using a production-style cloud architecture. The goal was to modernize infrastructure, improve security, and separate application and database layers for scalability and maintainability.
The application was deployed using Amazon EC2 and Amazon RDS, replacing a traditional single-server LAMP setup with a cloud-native design.
🏗 Architecture
Components Used:
Amazon EC2 (Ubuntu 24.04)
Amazon RDS (MySQL)
Apache Web Server
PHP
WordPress
AWS Security Groups
SSH Key Pair Authentication
Architecture Flow:
User → Internet → EC2 (Apache/PHP/WordPress) → RDS (MySQL)
Application and database tiers were separated to follow best practices for security and scalability.
🔐 Security Implementation
EC2 security group allows:
HTTP (80)
HTTPS (443)
SSH (22 – restricted to my IP)
RDS security group allows:
MySQL (3306) only from EC2 security group
Database credentials stored securely in wp-config.php
SSH key authentication used instead of password login
⚙️ Deployment Steps
Provisioned EC2 instance (Ubuntu)
Configured security groups
Created RDS MySQL instance
Installed Apache, PHP, and required packages
Connected EC2 to RDS
Created WordPress database
Configured WordPress to use RDS endpoint
Completed web-based WordPress installation
📈 Key Cloud Engineering Concepts Demonstrated
Infrastructure provisioning
Cloud networking & security groups
Application/database tier separation
Managed database services (RDS)
Linux server configuration
Secure SSH access
Cloud migration planning
