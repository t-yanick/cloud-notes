# Day 02 – AWS Global Infrastructure

## Course(s)
- Understanding AWS and its Global Infrastructure  
  Instructor: David Blocher  
  Platform: Pluralsight (Sep 2024)

- AWS Foundations (selected sections)  
  Instructor: David Blocher  
  Platform: Pluralsight

---

## What is AWS Global Infrastructure?
- Definition of AWS global infrastructure
- Why AWS operates infrastructure globally
- How global infrastructure supports scalability and resilience

---

## AWS Regions
- What an AWS Region is
- Why regions are geographically isolated
- Examples of AWS regions
- When and why to choose a specific region

### Canada Focus
- ca-central-1 (Montreal)
- Latency benefits for Canadian users
- Data residency and compliance considerations

---

## Availability Zones (AZs)
- What an Availability Zone is
- Relationship between AZs and data centers
- How AZs improve fault tolerance
- Difference between single-AZ vs multi-AZ architectures

---

## Edge Locations
- What edge locations are
- Purpose of edge locations (low latency)
- Relationship to Amazon CloudFront
- Difference between edge locations and regions

---

## How AWS Achieves High Availability
- Region-level isolation
- Multi-AZ design
- Load balancing across AZs
- Service redundancy

---

## Architecture Example
- Description of a highly available application
- Components used (ALB, EC2, AZs)
- Traffic flow from user to application

---

## IAM Overview (Foundations Preview)
- What IAM is
- Why IAM is critical for security
- Core components:
  - Users
  - Groups
  - Roles
  - Policies

---

## Hands-On (CLI – Read Only)
- Commands executed:
  - aws iam list-users
  - aws iam list-roles
  - aws ec2 describe-regions
  - aws ec2 describe-availability-zones --region ca-central-1
- Observations from command outputs

---

## Reflection
- Why AWS designs its infrastructure this way
- How regions and AZs influence application availability
- How this knowledge helps in cloud engineering and DevOps roles

---

## Key Takeaways
- Global infrastructure is the foundation of AWS services
- Region and AZ choices directly affect reliability and performance
- High availability is designed, not accidental
