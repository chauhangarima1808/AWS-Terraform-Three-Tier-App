# AWS-Terraform-Three-Tier-App

This project focuses on designing and deploying a highly scalable, highly available, and secure three-tier web application architecture on Amazon Web Services (AWS) using Terraform as the Infrastructure as Code (IaC) tool.

The three-tier architecture—comprising presentation (web), application (logic), and data (database) layers—is a widely adopted model for building robust, modular, and scalable applications. Leveraging AWS cloud-native services and Terraform automation, this project showcases how to build and manage modern cloud infrastructure that is production-ready.

## Project Highlights
- Infrastructure Provisioning with Terraform: Automated provisioning of all AWS resources including VPC, subnets, security groups, EC2 instances, RDS, and load balancers using modular and reusable Terraform code.
- Scalability & High Availability: Designed with Auto Scaling Groups, Multi-AZ deployment, and Elastic Load Balancing to ensure seamless scaling and fault tolerance.
- Security Best Practices: Network segmentation using public/private subnets, IAM roles and policies, security groups, and encrypted storage for data at rest.
- Monitoring & Logging: Integration with AWS CloudWatch for real-time monitoring, logging, and alarms for operational visibility.
- Modular Architecture: Clear separation of concerns using Terraform modules to promote reusability, scalability, and ease of maintenance.

## Architecture

### Target architecture
![Architecture Diagram](/architecture.jpg "Architecture Diagram")

### Target technology stack 
- **Amazon VPC** Provides secure networking for resources.
- **Amazon EC2**  Offers scalable compute capacity for hosting applications.
- **Amazon RDS**  Simplifies database management with high availability.
- **Amazon EFS**  Enables scalable and shared storage for the application.
- **NAT Gateway**  Provides secure internet access for instances residing in private subnets.
- **Application Load Balancer**  Distributes traffic efficiently for fault tolerance.
- **IAM (Identity and Access Management)**  using IAM roles are assigned to nodes in the EKS cluster to ensure secure access control.

### Setting Up the Amazon VPC:
- Designed a custom VPC with public and private subnets for optimal security.
- Configured routing tables, NAT gateways, and internet gateways to manage traffic flow.
- Implemented security groups to control access to resources.
  
### Configuring Amazon EC2 for Compute Resources:
- Launched EC2 instances in the private subnet to host the application.
- Configured auto-scaling groups to ensure the application could handle variable traffic loads.
- Used Application Load Balancer (ALB) to distribute traffic across instances for high availability.
  
### Deploying Amazon RDS for Database Management:
- Set up a managed relational database using Amazon RDS.
- Configured Multi-AZ deployment for automatic failover and data redundancy.
- Optimized performance with read replicas for handling read-heavy workloads.

### Integrating Amazon EFS for Shared Storage:
- Created an Amazon EFS file system for shared and scalable storage.
- Mounted EFS on EC2 instances to enable seamless file sharing across the application.
- Ensured high availability by deploying EFS across multiple Availability Zones.
  
## Key Learnings
- Design for Redundancy: Use Multi-AZ deployments and load balancers to avoid single points of failure.<br>
- Automate Scaling: Leverage auto-scaling to handle variable traffic loads.<br>
- Secure Resources: Implement security groups, IAM roles, and encryption for data protection.<br>
- Monitor Continuously: Use tools like CloudWatch to track application health and performance.

## Conclusion
This project successfully demonstrates the power of Infrastructure as Code with Terraform and the scalability of AWS in deploying a secure, resilient, and production-ready three-tier web application. By leveraging modular design, automation, and AWS best practices, the solution ensures high availability, seamless scalability, and operational efficiency—making it a solid foundation for modern cloud-native applications.
