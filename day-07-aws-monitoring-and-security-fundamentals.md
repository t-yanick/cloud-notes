# Day 7 — AWS Monitoring & Security Fundamentals

## Overview
Day 7 focused on operational visibility and security principles in AWS. Although the modules were short, they covered foundational concepts that are critical for maintaining reliable, secure, and production-ready cloud environments.

Monitoring and security are core responsibilities of cloud engineers, not optional enhancements.

---

# Part 1 — AWS Monitoring Fundamentals

## Amazon CloudWatch

CloudWatch is AWS’s primary monitoring and observability service.

### Core Capabilities
- Metrics collection
- Log aggregation
- Alarms and notifications
- Event-driven automation
- Dashboards for visualization

---

## Metrics

Metrics are time-ordered data points collected from AWS services.

### Examples:
- EC2 CPU utilization
- Network In/Out
- Disk read/write operations
- RDS CPU usage

Metrics help identify:
- Performance bottlenecks
- Scaling needs
- Service degradation

---

## Logs

CloudWatch Logs allow:
- Centralized log storage
- Real-time monitoring
- Log retention configuration

Used for:
- Application debugging
- Audit trails
- Incident investigation

---

## Alarms

CloudWatch Alarms:
- Trigger when thresholds are crossed
- Can notify via SNS
- Can trigger automated scaling or recovery actions

Example:
- CPU > 80% for 5 minutes → scale out

---

## Observability Perspective

Monitoring answers:
- Is the system healthy?
- Is it performing as expected?
- Is it failing silently?

Observability is essential for:
- Reliability
- Cost control
- Incident response

---

# Part 2 — AWS Security & Compliance Fundamentals

## Shared Responsibility Model

One of the most important AWS security concepts.

### AWS Responsibility:
- Physical data centers
- Hardware
- Global infrastructure
- Managed services security

### Customer Responsibility:
- Data protection
- IAM configuration
- Network configuration
- Operating system patching (EC2)
- Application security

---

## Identity and Access Management (IAM)

Security in AWS begins with identity.

Key principles:
- Least privilege
- Role-based access
- Avoid root account usage
- Avoid long-lived access keys

IAM controls:
- Who can access resources
- What actions they can perform

---

## Encryption

AWS supports encryption:

### At Rest:
- S3 encryption (SSE-S3, SSE-KMS)
- EBS encryption
- RDS encryption

### In Transit:
- TLS/HTTPS
- Encrypted API endpoints

Encryption protects sensitive data from unauthorized access.

---

## Network Security

- Security Groups → Instance-level firewall (stateful)
- Network ACLs → Subnet-level filtering (stateless)

Best practices:
- Restrict inbound traffic
- Avoid 0.0.0.0/0 unless necessary
- Limit SSH access

---

## Compliance & Governance

AWS supports compliance frameworks such as:
- ISO
- SOC
- PCI-DSS
- HIPAA (depending on configuration)

However:
Compliance responsibility is shared and depends on proper configuration.

---

# Engineering Takeaways

- Monitoring ensures operational reliability.
- Security must be designed into infrastructure, not added later.
- Least privilege and encryption are foundational principles.
- Cloud engineers are responsible for observability and secure configuration.

---

## Portfolio Summary

Completed foundational study of AWS monitoring and security principles. Developed understanding of CloudWatch metrics and alarms, the Shared Responsibility Model, IAM best practices, encryption standards, and secure network configuration principles.

---

## Status

AWS Core Foundations Path Completed.
