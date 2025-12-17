# Day 3 – AWS Foundations

This document consolidates core AWS concepts learned from multiple foundational courses into a single, structured reference.  
The focus is on **conceptual understanding**, **system thinking**, and **practical relevance**, rather than course-by-course summaries.

---

## 1. AWS Management Console

**Source**  
*Getting Started with the AWS Management Console*  
Michael Cassidy — Aug 2024

### Key Points
- The AWS Management Console is a web-based interface for managing AWS services
- Resources are created and managed within a selected AWS Region
- Useful for learning, exploration, and troubleshooting
- Not ideal for large-scale or repeatable production workflows
- Infrastructure as Code (IaC) tools are preferred for automation and consistency

---

## 2. Identity and Access Management (IAM)

**Source**  
*AWS Identity and Access Management Fundamentals*  
Neil Hitchins — Aug 2024

### Key Points
- IAM controls authentication and authorization across AWS
- Core IAM entities:
  - **Users:** human identities
  - **Groups:** permission management
  - **Roles:** temporary, service-based access
- Permissions are defined using JSON policies
- Follows the **principle of least privilege**
- IAM roles are preferred over long-lived access keys for security

---

## 3. Compute Fundamentals (EC2)

**Source**  
*AWS Compute Fundamentals* + *Create and Connect to an EC2 Instance (Hands-on Lab)*  
Neil Hitchins / Beth Hord — 2024–2025

### Key Points
- EC2 provides resizable virtual servers in the cloud
- Instances are launched from Amazon Machine Images (AMIs)
- SSH is used for secure, key-based access
- Security Groups act as stateful virtual firewalls
- SCP enables secure file transfer over SSH
- EC2 is a foundational building block for many higher-level AWS services

---

## 4. Networking Fundamentals

**Source**  
*AWS Networking Fundamentals*  
Neil Hitchins — Oct 2024

### Key Points
- A Virtual Private Cloud (VPC) is a logically isolated network
- Core networking components:
  - Subnets (public and private)
  - Route tables
  - Internet Gateway
  - Security Groups
  - Network ACLs
- Availability Zones enable fault tolerance and high availability
- Load balancers distribute traffic across resources and AZs

---

## 5. Storage Fundamentals

**Source**  
*AWS Storage Fundamentals*  
Neil Hitchins — Nov 2024

### Key Points
- **Amazon S3:** object storage for static assets, backups, and data lakes
- **EBS:** block storage for EC2 instances
- **EFS:** shared file systems for multiple EC2 instances
- Storage choice depends on access pattern, durability, and performance needs

---

## 6. Database Fundamentals

**Source**  
*AWS Database Fundamentals*  
Beth Hord — Nov 2024

### Key Points
- **Amazon RDS:** managed relational databases
- **DynamoDB:** fully managed NoSQL key-value store
- Multi-AZ deployments improve availability and resilience
- Managed databases reduce operational and maintenance overhead

---

## 7. Monitoring and Observability

**Source**  
*AWS Monitoring Fundamentals*  
Neil Hitchins — Dec 2024

### Key Points
- Amazon CloudWatch provides metrics, logs, and events
- Metrics offer insight into system performance and health
- Alarms trigger notifications or automated responses
- Observability is essential for reliability, scaling, and troubleshooting

---

## 8. Security and Compliance

**Source**  
*AWS Security and Compliance Fundamentals*  
Beth Hord — Jan 2025

### Key Points
- AWS follows the **Shared Responsibility Model**
  - AWS secures the cloud infrastructure
  - Customers secure workloads and data
- Security is implemented using a layered (defense-in-depth) approach
- Encryption supported at rest and in transit
- AWS supports multiple compliance standards and regulatory frameworks

---

## 9. Machine Learning and AI (High-Level Overview)

**Source**  
*AWS Machine Learning and Artificial Intelligence Fundamentals*  
Noreen Hasan — Sept 2024

### Key Points
- AWS provides managed AI/ML services
- Abstracts infrastructure management
- Enables inference, automation, and analytics
- ML services complement traditional cloud workloads rather than replace them

---

## Reflection

- AWS services are modular and composable
- Real-world architectures combine compute, networking, storage, security, and monitoring
- Manual console usage is useful for learning but does not scale
- Automation and Infrastructure as Code are essential for production environments

---

## Status
✅ Day 3 – AWS Foundations completed
