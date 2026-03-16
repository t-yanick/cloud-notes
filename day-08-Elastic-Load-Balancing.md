# Day 8 – Elastic Load Balancing

## Overview
This module explored how AWS distributes traffic across multiple compute resources using Elastic Load Balancing (ELB). Load balancing improves application availability, fault tolerance, and scalability.

Topics covered:
- Review of AWS Global Infrastructure
- Introduction to Elastic Load Balancing
- Application Load Balancer (ALB)
- Network Load Balancer (NLB)
- Gateway Load Balancer (GWLB)
- Load balancer optimization techniques
- HTTPS listener configuration
- Practical demos for ALB and NLB

---

# AWS Global Infrastructure Review

AWS infrastructure is organized into:

## Regions
A geographic area containing multiple data centers.

Example:
- us-east-1
- eu-west-1

## Availability Zones
Independent data centers within a region designed for fault isolation.

High availability is achieved by deploying resources across multiple AZs.

## Edge Locations
Used for content delivery and caching through services like CloudFront.

Load balancers typically operate within a region but distribute traffic across multiple availability zones.

---

# Introduction to Elastic Load Balancing

Elastic Load Balancing automatically distributes incoming application traffic across multiple targets.

Targets may include:
- EC2 instances
- Containers
- IP addresses
- Lambda functions

Benefits of ELB:

- High availability
- Fault tolerance
- Automatic traffic distribution
- Integration with Auto Scaling
- SSL/TLS termination

---

# Types of AWS Load Balancers

AWS provides four main load balancers:

1. Application Load Balancer (ALB)
2. Network Load Balancer (NLB)
3. Gateway Load Balancer (GWLB)
4. Classic Load Balancer (legacy)

The course focused on ALB, NLB, and GWLB.

---

# Application Load Balancer (ALB)

Application Load Balancer operates at **Layer 7 (Application Layer)**.

It routes traffic based on HTTP request data such as:

- URL path
- Host headers
- Query strings

Example routing:

/api → API service  
/images → image server  
/app → web application

Key features:

- Path-based routing
- Host-based routing
- Integration with containers
- WebSocket support
- HTTP/HTTPS support

---

# ALB Architecture

Typical flow:

User Request  
↓  
Application Load Balancer  
↓  
Target Group  
↓  
EC2 Instances

Each target group contains backend resources and performs health checks.

---

# ALB Setup Demonstration

Steps demonstrated in the lab:

1. Create an Application Load Balancer
2. Configure listener (HTTP or HTTPS)
3. Create target group
4. Register EC2 instances
5. Configure routing rules
6. Test application accessibility

The ALB distributes traffic evenly across healthy targets.

---

# Network Load Balancer (NLB)

Network Load Balancer operates at **Layer 4 (Transport Layer)**.

It handles:

- TCP
- UDP
- TLS

NLB is designed for:

- extremely high performance
- ultra-low latency
- millions of requests per second

Key characteristics:

- static IP addresses
- very fast throughput
- minimal latency

---

# NLB Setup Demonstration

Steps demonstrated:

1. Create a Network Load Balancer
2. Configure TCP listener
3. Create target group
4. Register instances
5. Test connectivity

Unlike ALB, NLB does not inspect HTTP content.

---

# Gateway Load Balancer (GWLB)

Gateway Load Balancer is designed for **network security appliances**.

Examples:

- firewalls
- intrusion detection systems
- packet inspection tools

GWLB combines:

- transparent network gateway
- load balancing for security appliances

It allows security services to scale horizontally.

---

# HTTPS Listener Configuration

Load balancers can terminate SSL/TLS connections.

Benefits:

- encryption between client and load balancer
- simplified certificate management
- reduced workload on backend servers

Steps demonstrated:

1. Create HTTPS listener (port 443)
2. Attach SSL certificate
3. Configure target group
4. Route secure traffic to backend instances

Certificates are typically managed using:

AWS Certificate Manager.

---

# Load Balancer Optimization Techniques

Several strategies improve load balancing efficiency.

## Cross-Zone Load Balancing

Distributes traffic evenly across instances in different availability zones.

This prevents uneven traffic distribution.

---

## Health Checks

Load balancers continuously monitor instance health.

If a target fails:

- it is removed from rotation
- traffic is redirected to healthy targets

---

## Sticky Sessions

Allows requests from the same client to be routed to the same backend server.

Useful for applications that maintain session state.

---

# Integration with Auto Scaling

Load balancers commonly work with Auto Scaling Groups.

Architecture pattern:

Internet  
↓  
Load Balancer  
↓  
Auto Scaling Group  
↓  
EC2 Instances across multiple AZs

This enables:

- automatic scaling
- high availability
- fault tolerance

---

# Exam Tips

Important concepts for the SAA exam:

- ALB operates at Layer 7
- NLB operates at Layer 4
- GWLB is used for security appliances
- Load balancers improve availability across multiple AZs
- Health checks automatically remove unhealthy instances
- SSL termination can be handled by the load balancer

---

# Key Takeaways

- Elastic Load Balancing distributes traffic across multiple resources.
- ALB enables intelligent HTTP routing.
- NLB provides extremely high network performance.
- GWLB allows scaling of security appliances.
- Load balancers combined with Auto Scaling create highly resilient architectures.