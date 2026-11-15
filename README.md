Secure 2-Tier Web Application on AWS

A Cloud and DevOps learning project focused on deploying a Django web application on AWS, integrating a managed MySQL database, configuring cloud networking and security, and exploring deployment automation and infrastructure management.

Project Overview

This project demonstrates the deployment of a Django-based web application using Amazon Web Services (AWS).

The application was deployed on an Ubuntu-based Amazon EC2 instance using Nginx and Gunicorn, with Amazon RDS for MySQL as the managed database service.

The project also includes practical exploration of AWS networking, security groups, Docker, GitHub Actions, Terraform, CloudWatch, load balancing, and Auto Scaling.

«Current Status: AWS resources used during testing have been deleted to avoid unnecessary costs. The application is not currently live on AWS.»

Architecture

Architecture Type: 2-Tier Architecture

              Users
                |
                v
             Internet
                |
                v
              AWS VPC
                |
                v
          Amazon EC2
          Ubuntu Linux
                |
          +-----+------+
          |            |
         Nginx      Gunicorn
                       |
                       v
                  Django App
                       |
                       v
                 Amazon RDS
                   MySQL

Application Tier

- Amazon EC2 (Ubuntu Linux)
- Nginx as a reverse proxy
- Gunicorn application server
- Django web application

Database Tier

- Amazon RDS
- MySQL database
- Database connectivity through AWS security configurations

Architecture Note: The tested application used a single EC2 application server connected to an RDS MySQL database configured as Single-AZ. Application Load Balancer, Target Groups, Auto Scaling, and CloudWatch alarms were configured and tested separately. They were not part of the final application traffic path.

Technologies and AWS Services

Technology / Service| Purpose
AWS| Cloud infrastructure
Amazon EC2| Application hosting
Amazon RDS (MySQL)| Managed database
Amazon VPC| Network isolation
Subnets| Network segmentation
Route Tables| Network routing
Internet Gateway| Internet connectivity
Security Groups| Traffic access control
IAM| Identity and access management
Ubuntu Linux| Server operating system
Python and Django| Backend application
Nginx| Reverse proxy
Gunicorn| Application server
Docker| Containerization
Git and GitHub| Version control
GitHub Actions| CI/CD automation
Terraform| Infrastructure as Code exploration
Amazon CloudWatch| Monitoring
Application Load Balancer| Load balancing experiments
EC2 Auto Scaling| Scaling experiments

Key Implementations

1. AWS Infrastructure and Networking

- Created and configured a custom VPC.
- Worked with public and private subnet concepts.
- Configured route tables and an Internet Gateway.
- Created Security Groups and configured traffic rules.

2. Application Deployment

- Launched an Ubuntu EC2 instance.
- Deployed the Django application.
- Configured Nginx as a reverse proxy.
- Used Gunicorn to serve the Django application.
- Connected the application to Amazon RDS MySQL.

3. Database Management

- Created an Amazon RDS MySQL database.
- Configured database connectivity and security group rules.
- Used managed database hosting for the AWS deployment.

4. Docker

- Created a Dockerfile for the Django application.
- Explored Docker-based application packaging and containerization.

5. CI/CD with GitHub Actions

- Created GitHub Actions workflows.
- Worked on deployment automation.
- Explored AWS Systems Manager-based deployment.
- Tested workflow execution and troubleshooting.

6. Terraform

- Worked with Terraform configuration files.
- Explored the AWS provider and infrastructure data sources.
- Practised Infrastructure as Code concepts.

Full Terraform-based infrastructure provisioning was not verified as completed.

7. Load Balancing and Auto Scaling

- Configured and tested an Application Load Balancer and Target Group.
- Tested EC2 Auto Scaling by scaling from one instance to two and back to one.
- Explored instance health and traffic distribution concepts.
- These components were tested separately and subsequently removed.

8. CloudWatch Monitoring

- Explored CloudWatch dashboards and monitoring.
- Configured monitoring and scaling-related alarms.
- Studied application health and infrastructure monitoring concepts.

Repository Structure

secure-2-tier-web-application/
│
├── .github/
│   └── workflows/
│
├── config/
├── core/
├── terraform/
│
├── Dockerfile
├── .dockerignore
├── .gitignore
├── manage.py
├── requirements.txt
├── README.md
│
└── Secure-2-Tier-Web-Application-Public-Safe.pdf

Project Documentation

The complete project documentation contains 26 screenshots showing AWS infrastructure configuration, application deployment, database setup, networking, monitoring, Docker, GitHub Actions, and Terraform work.

<details>
<summary><b>View documentation details</b></summary>- AWS Management Console and VPC configuration
- Subnets and route tables
- Security Groups
- EC2 instances and Auto Scaling experiments
- Load Balancer and Target Groups
- Amazon RDS MySQL
- Django application running during testing
- CloudWatch monitoring
- GitHub repository and Dockerfile
- GitHub Actions workflow
- Terraform configuration

</details>"View Project Screenshots and Documentation (PDF)" (Secure-2-Tier-Web-Application-Public-Safe.pdf)

Sensitive account identifiers, public IP addresses, and database endpoints have been redacted in the public documentation.

Security Practices

- Used a dedicated VPC for project networking.
- Configured Security Groups to control network traffic.
- Explored public and private subnet configurations.
- Used Amazon RDS for managed database hosting.
- Explored IAM and AWS Systems Manager access concepts.
- Avoided publishing credentials and sensitive AWS account information.

This is an educational project, not a complete production security audit.

Cost Management

AWS resources were deleted after testing to avoid unnecessary ongoing charges.

The cleanup included the main EC2, RDS, load balancing, Auto Scaling, monitoring, and networking resources used during the project.

Historical usage may still appear in AWS billing reports after resource deletion.

Key Learning Outcomes

- AWS cloud infrastructure and networking.
- Linux server administration using Ubuntu.
- Django application deployment on EC2.
- Nginx and Gunicorn configuration.
- Amazon RDS MySQL integration.
- AWS Security Groups and access management.
- Docker fundamentals.
- GitHub Actions and CI/CD workflows.
- Terraform fundamentals.
- CloudWatch monitoring.
- Auto Scaling and load balancing concepts.
- AWS cost monitoring and resource cleanup.

Future Improvements

- Complete and validate Terraform-based infrastructure provisioning.
- Improve automated deployment validation.
- Strengthen application security and secret management.
- Explore highly available and Multi-AZ architectures.
- Expand container-based deployment practices.

Author

Aman Yadav

BCA Student | Aspiring Cloud & DevOps Engineer

- GitHub: "AMANYADAV162" (https://github.com/AMANYADAV162)
- Project Repository: "Secure 2-Tier Web Application" (https://github.com/AMANYADAV162/secure-2-tier-web-application)

---

Built as a hands-on learning project to gain practical experience with AWS, Linux, Django, cloud networking, and DevOps tools.
