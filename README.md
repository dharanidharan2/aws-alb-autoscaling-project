# AWS ALB Auto Scaling Project

## Project Overview

This project demonstrates a highly available and scalable web application architecture on AWS using:

* Amazon EC2
* Auto Scaling Group (ASG)
* Application Load Balancer (ALB)
* Target Group
* Launch Template
* VPC
* Public Subnets

## Architecture

Internet → Application Load Balancer → Target Group → EC2 Instances → Auto Scaling Group

## AWS Services Used

* Amazon EC2
* Amazon VPC
* Application Load Balancer
* Target Group
* Auto Scaling Group
* Launch Template
* Security Groups

## Configuration

### VPC

* CIDR: 10.0.0.0/16

### Public Subnets

* Public-Subnet-A
* Public-Subnet-B

### Auto Scaling Group

* Desired Capacity: 2
* Minimum Capacity: 2
* Maximum Capacity: 4

### Load Balancer

* Application Load Balancer (ALB)
* HTTP Port 80

## Validation

* Verified ALB accessibility
* Verified healthy target group instances
* Verified Auto Scaling deployment
* Verified multi-Availability Zone architecture

## Outcome

Successfully deployed a highly available and scalable AWS infrastructure using ALB and Auto Scaling Group.
