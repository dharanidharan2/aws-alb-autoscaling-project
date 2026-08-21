# AWS ALB Auto Scaling Project

## Overview

This project demonstrates the deployment of a highly available and scalable web infrastructure on AWS using Application Load Balancer (ALB), Auto Scaling Group (ASG), EC2 Instances, Launch Templates, and a custom VPC.

The architecture is designed to distribute traffic across multiple Availability Zones and automatically replace unhealthy instances to ensure high availability.

## Architecture

```text
Internet
    │
    ▼
Application Load Balancer (ALB)
    │
    ▼
Target Group
    │
 ┌──┴──┐
 ▼     ▼
EC2   EC2
AZ-A  AZ-B
    │
    ▼
Auto Scaling Group
(Min: 2 | Desired: 2 | Max: 4)
```

## AWS Services Used

* Amazon EC2
* Amazon VPC
* Application Load Balancer (ALB)
* Target Group
* Auto Scaling Group (ASG)
* Launch Template
* Security Groups
* Elastic Load Balancing (ELB)

## Infrastructure Configuration

### VPC

* Name: production-vpc
* CIDR Block: 10.0.0.0/16

### Public Subnets

* Public-Subnet-A (ap-south-1a)
* Public-Subnet-B (ap-south-1b)

### Launch Template

* Name: production-template
* AMI: Amazon Linux 2023
* Instance Type: t3.micro

### Auto Scaling Group

* Name: production-asg
* Desired Capacity: 2
* Minimum Capacity: 2
* Maximum Capacity: 4

### Load Balancer

* Name: Production-ALB
* Type: Application Load Balancer
* Protocol: HTTP
* Port: 80

### Target Group

* Name: productiontg
* Protocol: HTTP
* Port: 80

## Health Checks

The Target Group continuously monitors instance health.

* EC2 Health Checks Enabled
* ELB Health Checks Enabled
* Automatic unhealthy instance replacement through Auto Scaling

## Validation Performed

* Successfully created custom VPC and subnets
* Configured Application Load Balancer
* Created Target Group and registered instances
* Created Launch Template
* Configured Auto Scaling Group across multiple Availability Zones
* Verified healthy targets in Target Group
* Accessed application successfully using ALB DNS Name
* Confirmed high availability architecture

## Project Outcome

Successfully deployed a production-style AWS infrastructure that provides:

* High Availability
* Load Balancing
* Auto Scaling
* Fault Tolerance
* Multi-AZ Deployment

## Skills Demonstrated

* AWS EC2
* AWS VPC
* AWS Auto Scaling
* AWS Load Balancing
* AWS Networking
* Security Groups
* High Availability Architecture
* Cloud Infrastructure Management

## Author

Dharanidharan V

AWS Cloud Engineer
