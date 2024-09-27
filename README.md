# AWS-3-TIER-ARCHITECTURE

## Description: 
In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.

## Architecture Diagram
![Architecture Diagram](https://github.com/Ryanixon/AWS-3-TIER-ARCHITECTURE/blob/4ef7e358bfdb08fd282c8c6841c464d5f43e516a/3TierArchitecture.png)
  

## Pre-requisites:
1. An AWS account. If you don’t have an AWS account, follow the instructions [here](https://aws.amazon.com/console/) and
click on “Create an AWS Account” button in the top right corner to create one.
2. IDE or text editor of your choice.

## Features:
1. Scalable Architecture: Designed with scalability in mind, leveraging AWS services like Auto Scaling and Elastic Load Balancer (ELB).
2. Infrastructure as Code (IaC): Uses AWS CloudFormation or Terraform to provision resources such as EC2 instances, RDS, S3, and VPC.
3. High Availability: Multi-AZ (Availability Zones) setup for the application and database ensures redundancy.
4. Secure: Implements AWS IAM roles, Security Groups, and Network ACLs for secure communication and data protection.

## AWS Services Used
1. Amazon EC2: For hosting the application layer.
2. Amazon RDS: To manage the relational database.
3. Amazon S3: For static file storage.
4. Amazon VPC: For network isolation and security.
5. Amazon Route 53: For DNS routing.
6. Elastic Load Balancing (ELB): For distributing traffic across instances.
7. AWS Auto Scaling: To dynamically scale resources based on traffic.


