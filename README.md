# AWS Scalable Web Application Project

# GRADUTION PROJECT FOR MANARA PROGRAM FOR AWS SAA C-03

##  Project Overview

This project demonstrates the deployment of a scalable and highly available web application on AWS using EC2 instances, Application Load Balancer (ALB), and Auto Scaling Groups (ASG). It follows best practices for compute scalability, security, and cost optimization.

---

##  Architecture

**Type**: EC2-based

The architecture includes the following core components:

- **Amazon EC2**: Hosts the web application on virtual servers.
- **Application Load Balancer (ALB)**: Routes traffic evenly across EC2 instances.
- **Auto Scaling Group (ASG)**: Automatically adds/removes EC2 instances based on load.
- **Amazon RDS (optional)**: Provides a managed relational database service (MySQL/PostgreSQL).
- **IAM Roles**: Secure access to AWS services for EC2 and other components.
- **CloudWatch + SNS**: Logs, monitors, and sends notifications based on metrics.

---

##  Architecture Diagram

![Architecture Diagram](https://github.com/abdelrhmanmohamed1234/Scalable-Web-Application-with-ALB-and-Auto-Scaling/blob/main/project_digram.gif)

---

##  Deployment Steps

> You can deploy the infrastructure manually via the AWS Console or use Infrastructure as Code (e.g., Terraform or CloudFormation).

### 1. Launch EC2 Instances
- Choose Amazon Linux 2 or Ubuntu
- Install a simple web server (e.g., Apache, Nginx)
- Create a custom AMI if needed

### 2. Create a Target Group and ALB
- Register EC2 instances with the target group
- Configure listeners and health checks

### 3. Configure Auto Scaling Group
- Attach it to the ALB target group
- Set scaling policies (CPU > 60% → scale out)

### 4. (Optional) Launch RDS Database
- Multi-AZ deployment
- Connect from EC2 instances using internal endpoint

### 5. Set IAM Roles
- Assign roles to EC2 for access to logs, S3, etc.

### 6. Enable CloudWatch & SNS
- Set alarms for metrics like CPUUtilization
- Send alerts to email via SNS topic

---

##  Tools and Services

| Service         | Purpose                           |
|----------------|-----------------------------------|
| Amazon EC2      | Hosts the web application         |
| ALB             | Distributes traffic               |
| ASG             | Handles scalability               |
| Amazon RDS      | Backend database (optional)       |
| IAM             | Access control                    |
| CloudWatch      | Monitoring and logging            |
| SNS             | Notifications                     |

---

##  Learning Outcomes

- Configure and deploy a secure EC2-based web application
- Set up high availability using ALB and ASG
- Optimize cost and performance using scaling policies
- Integrate monitoring and alerting via CloudWatch and SNS

---



