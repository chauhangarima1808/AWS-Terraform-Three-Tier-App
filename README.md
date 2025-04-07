# AWS-Terraform-Three-Tier-App

A comprehensive project deploying a sample web application using Terraform EKS modules and add-ons. My focus was on establishing robust networking, efficient cluster provisioning, essential add-ons, and comprehensive monitoring to ensure a seamless deployment experience. The solution includes a multi-AZ VPC with private and public subnets, Amazon EKS running across private subnets, ELB for traffic routing, auto-scaling for dynamic capacity management, and CloudWatch Observability for real-time monitoring.

## Project Highlights
- A multi-AZ VPC with private and public subnetsfor secure and scalable networking.
- Amazon EKS control plane and worker nodes running across private subnets.
- EKS Managed Node Groups with auto-scalingfor dynamic workload management.
- Elastic Load Balancer (ELB) for routing external traffic.
- CloudWatch Observability for real-time monitoring.

## Architecture

### Target architecture
![Architecture Diagram](/eks-architecture.png "Architecture Diagram")

### Target technology stack 
- **Amazon EKS (Elastic Kubernetes Service):** EKS clusters are provisioned and auto-scaling node groups are used to efficiently handle workloads.
- **VPC** A multi-AZ VPC with private and public subnets ensures secure, scalable networking for the EKS deployment.
- **NAT GATEWAYS** Used to allow outbound internet access for worker nodes in private subnets.
- **CloudWatch Container Insights** Collects metrics and logs from the EKS pods, enabling proactive monitoring of CPU, memory, and performance metrics.
- **EKS Add-ons** Enhance the Amazon EKS clusters with production-grade add-ons for networking, observability, security, and scalability using Terraform Blueprints.
- **IAM (Identity and Access Management)**  using IAM roles are assigned to nodes in the EKS cluster to ensure secure access control.

### 𝐁𝐮𝐢𝐥𝐝𝐢𝐧𝐠 𝐚 𝐍𝐞𝐭𝐰𝐨𝐫𝐤𝐢𝐧𝐠 𝐅𝐨𝐮𝐧𝐝𝐚𝐭𝐢𝐨𝐧 𝐰𝐢𝐭𝐡 𝐓𝐞𝐫𝐫𝐚𝐟𝐨𝐫𝐦:
- A multi-AZ network with private subnets for worker nodes.
- NAT Gateways to allow outbound internet access from private subnets.
- Security Groups and Network ACLs to control traffic between subnets, ensuring fine-grained access control and a secure environment.
  
### 𝐃𝐞𝐩𝐥𝐨𝐲𝐢𝐧𝐠 𝐚𝐧 𝐄𝐊𝐒 𝐂𝐥𝐮𝐬𝐭𝐞𝐫 𝐰𝐢𝐭𝐡 𝐓𝐞𝐫𝐫𝐚𝐟𝐨𝐫𝐦:
- Provisioning the EKS control plane in a dedicated VPC.
- Deploying worker nodes in auto-scaling groups across private subnets.
- IAM role assignments to securely manage cluster access.

### 𝐄𝐧𝐡𝐚𝐧𝐜𝐢𝐧𝐠 𝐄𝐊𝐒 𝐰𝐢𝐭𝐡 𝐓𝐞𝐫𝐫𝐚𝐟𝐨𝐫𝐦 𝐀𝐝𝐝-𝐨𝐧𝐬 𝐚𝐧𝐝 𝐍𝐚𝐭𝐢𝐯𝐞 𝐂𝐚𝐩𝐚𝐛𝐢𝐥𝐢𝐭𝐢𝐞𝐬:
- VPC-CNI for efficient pod networking within the VPC.
- CloudWatch Observability for real-time logs, metrics, and performance monitoring.
- AWS Load Balancer Controller for automated ALB/NLB provisioning and traffic management.

### 𝐈𝐧𝐭𝐞𝐠𝐫𝐚𝐭𝐢𝐧𝐠 𝐀𝐦𝐚𝐳𝐨𝐧 𝐄𝐊𝐒 𝐂𝐥𝐨𝐮𝐝𝐖𝐚𝐭𝐜𝐡 𝐂𝐨𝐧𝐭𝐚𝐢𝐧𝐞𝐫 𝐈𝐧𝐬𝐢𝐠𝐡𝐭𝐬:
- Tracking CPU and memory utilization per pod.
- Integrating logs and metrics for proactive monitoring and troubleshooting.
- Enhancing operational efficiency with real-time alerts and dashboards.
  
## Key Learnings
✔ Terraform simplifies infrastructure as code (IaC), making EKS and VPC deployments scalable and repeatable.
✔ A well-architected VPC with private subnets improves security and isolation.
✔ EKS Blueprints Add-ons optimize networking (VPC-CNI), observability (CloudWatch), AWS Load Balancer controller.
✔ CloudWatch Container Insights offers real-time monitoring for proactive issue resolution.

## Conclusion
This project demonstrates how to architect and deploy a production-ready Kubernetes environment on AWS using Terraform, with a strong focus on scalability, security, observability, and operational excellence. By leveraging Terraform EKS modules, VPC modules, and curated add-ons like VPC-CNI, CloudWatch, and the AWS Load Balancer Controller, we ensured a streamlined deployment experience and a resilient infrastructure foundation.

Through the integration of CloudWatch Container Insights, real-time visibility into cluster health and application performance is achieved, enabling proactive operations and rapid troubleshooting. The use of multi-AZ networking, private subnets, and IAM-based access control enhances both the reliability and security posture of the solution.

This end-to-end solution is not only scalable and cost-efficient but also adheres to AWS and Kubernetes best practices—making it an ideal blueprint for deploying containerized applications in enterprise environments.
