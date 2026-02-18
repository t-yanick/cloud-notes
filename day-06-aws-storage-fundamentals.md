# Day 6 — AWS Storage Fundamentals

## Overview
Day 6 focused on understanding AWS storage services and how they support cloud workloads. The session covered object, block, and file storage models, along with cost, durability, and performance considerations.

This marks completion of AWS foundational services and establishes a solid base for production-grade architecture design.

---

## Objectives
- Understand different storage models (object, block, file)
- Learn when to use S3, EBS, or EFS
- Review storage classes and lifecycle management
- Understand encryption and security controls
- Build storage decision-making intuition

---

# 1. Amazon S3 (Simple Storage Service)

## What It Is
S3 is highly durable object storage designed for scalability, availability, and cost efficiency.

## Core Concepts
- Buckets (globally unique names)
- Objects (data + metadata)
- Region-scoped buckets
- 11 9’s durability (99.999999999%)

## Storage Classes
- Standard
- Intelligent-Tiering
- Standard-IA
- One Zone-IA
- Glacier Instant Retrieval
- Glacier Flexible Retrieval
- Glacier Deep Archive

## Features
- Versioning
- Lifecycle policies
- Cross-region replication
- Server-side encryption (SSE-S3, SSE-KMS)
- Bucket policies and IAM integration
- Block public access settings

## Use Cases
- Static website hosting
- Backups
- Log storage
- Data lakes
- Media storage

---

# 2. Amazon EBS (Elastic Block Store)

## What It Is
Block storage attached to EC2 instances.

## Key Characteristics
- AZ-scoped
- Persistent storage
- Used for operating system disks and application data

## Volume Types
- gp3 (general purpose SSD)
- io1 / io2 (provisioned IOPS)
- st1 (throughput optimized HDD)
- sc1 (cold HDD)

## Features
- Snapshots (stored in S3)
- Encryption
- Resize volumes
- Attach/detach capability

## Use Cases
- EC2 root volume
- Databases
- Transactional systems

---

# 3. Amazon EFS (Elastic File System)

## What It Is
Fully managed file storage using NFS protocol.

## Key Characteristics
- Shared across multiple EC2 instances
- Multi-AZ availability
- Automatically scales

## Use Cases
- Shared application content
- Web server clusters
- CMS platforms

---

# 4. Storage Decision Matrix

| Use Case | Recommended Service |
|------------|--------------------|
| Static files | S3 |
| EC2 OS disk | EBS |
| Shared storage across instances | EFS |
| Long-term archive | S3 Glacier |
| High IOPS database | EBS io2 |

---

# Architecture Perspective

Storage selection depends on:
- Access pattern
- Performance requirements
- Cost sensitivity
- Availability requirements
- Sharing requirements

Understanding these trade-offs is critical for real-world cloud architecture.

---

## Portfolio Summary

Studied and implemented AWS storage services including S3, EBS, and EFS. Developed understanding of storage models (object, block, file), lifecycle management, encryption, and service selection based on workload requirements.

---

## Status
AWS Core Fundamentals Completed.
