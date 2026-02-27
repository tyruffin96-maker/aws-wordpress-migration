# AWS Legacy Application Migration Project

## Overview

This project demonstrates the migration of a legacy web application to AWS using a production-style, multi-tier cloud architecture.

The objective was to modernize infrastructure, improve security, and separate application and database layers to support scalability and maintainability.

The application was deployed using Amazon EC2 and Amazon RDS, replacing a traditional single-server LAMP setup with a cloud-native architecture.

---

## Architecture

### Components Used

- Amazon EC2 (Ubuntu 24.04)
- Amazon RDS (MySQL)
- Apache Web Server
- PHP
- WordPress
- AWS Security Groups
- SSH Key Pair Authentication

### Architecture Flow

User → Internet → EC2 (Apache/PHP/WordPress) → RDS (MySQL)

The application and database tiers were separated to follow cloud security and scalability best practices.

---

## Security Implementation

### EC2 Security Group
- HTTP (80)
- HTTPS (443)
- SSH (22 – restricted to my IP)

### RDS Security Group
- MySQL (3306) allowed only from EC2 security group

### Additional Security Controls
- Database credentials configured in wp-config.php
- SSH key-based authentication used instead of password login
- Public access restricted to required services only

---

## Deployment Steps

1. Provisioned EC2 instance (Ubuntu)
2. Configured security groups
3. Created RDS MySQL instance
4. Installed Apache, PHP, and required dependencies
5. Connected EC2 to RDS
6. Created WordPress database
7. Configured WordPress to use RDS endpoint
8. Completed web-based WordPress installation

---

## Key Cloud Engineering Concepts Demonstrated

- Infrastructure provisioning
- Cloud networking and security group configuration
- Application and database tier separation
- Managed database services (Amazon RDS)
- Linux server configuration
- Secure SSH access
- Cloud migration strategy

---

## Future Enhancements

- Application Load Balancer (ALB)
- Auto Scaling Group
- Infrastructure as Code (Terraform)
- Docker containerization
- HTTPS via AWS Certificate Manager
- CloudWatch monitoring integration
