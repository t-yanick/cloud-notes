Users
  |
Internet
  |
Application Load Balancer (Public Subnets)
  |
-----------------------------------------
|                |                      |
AZ-1             AZ-2
Public Subnet    Public Subnet
ALB ENI          ALB ENI
                 |
           Private Subnet        Private Subnet
           EC2 Instance          EC2 Instance
           EC2 Instance          EC2 Instance

# Day 5 — AWS VPC & EC2 Networking (Hands-On Infrastructure)

## Overview
On Day 5, I designed and deployed a custom AWS Virtual Private Cloud (VPC) and launched EC2 instances inside the custom network. This lab focused on understanding how AWS networking components work together to provide isolated, secure, and internet-connected infrastructure for compute workloads.

This session represents a transition from using default AWS resources to designing foundational cloud infrastructure.

---

## Objectives
- Create a custom VPC with defined CIDR addressing
- Design subnets for network segmentation
- Configure route tables for traffic control
- Attach an Internet Gateway for public internet access
- Launch EC2 instances into a custom VPC
- Validate connectivity and security group configuration

---

## Architecture Components Implemented

### 1. Custom VPC
- Created a custom VPC with a defined IPv4 CIDR block
- Established isolated virtual networking environment

**Key Concept:**
The VPC acts as a virtual data center in AWS, controlling IP addressing, routing, and network isolation.

---

### 2. Subnets
- Created multiple subnets within the VPC
- Designed subnet layout to support public and private resource separation

**Key Concept:**
Subnet segmentation allows isolation of workloads and separation of internet-facing and backend resources.

---

### 3. Route Tables
- Created custom route tables
- Associated route tables with subnets
- Configured routes to control traffic flow

**Key Concept:**
A subnet is considered public or private based on its route table, not by its name.

---

### 4. Internet Gateway (IGW)
- Created and attached an Internet Gateway to the VPC
- Added default routes to enable outbound internet connectivity

**Traffic Flow:**
EC2 Instance → Subnet → Route Table → Internet Gateway → Internet


---

### 5. EC2 Deployment in Custom VPC
- Launched EC2 instances into specific subnets within the VPC
- Selected subnet and VPC during instance creation

**Key Concept:**
EC2 instances are deployed inside a VPC. The VPC provides the networking environment for EC2.

---

### 6. Public IP and Security Groups
- Enabled auto-assign public IPv4 for public subnet instances
- Configured security groups to allow required inbound access (e.g., SSH, HTTP)

**Key Concept:**
Security groups act as virtual firewalls controlling inbound and outbound traffic at the instance level.

---

## Architecture Hierarchy (Mental Model)

AWS Region
└── VPC
└── Subnets
└── EC2 Instances


This hierarchy reinforces that EC2 resources depend on VPC networking infrastructure.

---

## Key Skills Demonstrated
- AWS VPC design and configuration
- Subnet architecture and segmentation
- Route table management
- Internet Gateway configuration
- EC2 networking integration
- Basic cloud network security principles

---

## Portfolio Summary
Designed and deployed a custom AWS VPC with segmented subnets, configured route tables and an Internet Gateway for controlled internet access, and launched EC2 instances into the custom network. Implemented foundational AWS networking concepts including CIDR addressing, subnet routing, and public internet connectivity for compute workloads.

---

## Next Steps (Day 6 Preview)
- Implement NAT Gateway for private subnet outbound access
- Configure Application Load Balancer (ALB)
- Deploy EC2 instances across multiple Availability Zones
- Configure Auto Scaling Group for high availability
