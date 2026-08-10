# AWS-secure-vpc-project
Provides an isolated virtual network in AWS

## Project Overview

This project demonstrates the creation of a secure Virtual Private Cloud (VPC) in Amazon Web Services (AWS). It covers the fundamental networking components required to deploy a secure cloud environment following AWS best practices.

The objective of this project is to understand AWS networking concepts such as VPCs, subnets, route tables, Internet Gateway, Security Groups, and EC2 deployment.

---

## Project Architecture

![Architecture](architecture.png)

---

## Services Used

- Amazon VPC
- Public Subnet
- Route Table
- Internet Gateway (IGW)
- Security Groups
- Amazon EC2
- AWS Management Console

---

## Project Components

### 1. Virtual Private Cloud (VPC)

- Created a custom VPC (testcloudsecurity-VPC)
- CIDR Block: `10.0.0.0/16`
- Provides an isolated virtual network for AWS resources.

Screenshot:

`screenshots/vpc.png`

---

### 2. Public Subnet

- Created a public subnet inside the VPC.
- CIDR Block: `10.0.1.0/24`
- Configured to assign public IPv4 addresses automatically.

Screenshot:

`screenshots/subnets.png`

---

### 3. Internet Gateway

- Created and attached an Internet Gateway to the VPC.
- Allows communication between resources inside the VPC and the Internet.

Screenshot:

`screenshots/internet-gateway.png`

---

### 4. Route Table

Configured a custom route table with:

| Destination | Target |
|-------------|--------|
| 10.0.0.0/16 | Local |
| 0.0.0.0/0 | Internet Gateway |

Associated the route table with the public subnet.

Screenshot:

`screenshots/route-table.png`

---

### 5. Security Group

Created a Security Group to allow secure inbound traffic.

Allowed inbound rules:

- SSH (22) - My IP
- HTTP (80)
- HTTPS (443)

Outbound:

- Allow all traffic

Screenshot:

`screenshots/security-group.png`

---

### 6. EC2 Instance

Launched an Amazon Linux EC2 instance inside the public subnet.

Verified:

- Public IP assignment
- SSH connectivity
- Internet access

Screenshot:

`screenshots/ec2-instance.png`

---

## Skills Demonstrated

- AWS Networking Fundamentals
- Virtual Private Cloud (VPC)
- Subnet Design
- Internet Gateway Configuration
- Route Table Configuration
- Security Group Management
- EC2 Deployment
- Cloud Networking Basics

---

## Learning Outcomes

Through this project I learned:

- How AWS networking works.
- Difference between VPC and Subnets.
- How Internet Gateway provides Internet connectivity.
- How Route Tables control network traffic.
- How Security Groups act as virtual firewalls.
- How to launch an EC2 instance inside a custom VPC.
- Basic cloud security best practices.

---
## Future Improvements

- Add a private subnet
- Deploy a NAT Gateway
- Configure Network ACLs
- Enable VPC Flow Logs
- Create IAM Roles for EC2
- Implement least privilege security
- Deploy a web server inside the VPC

---

## Author

**Raj Kumar**

Aspiring Cloud Security Engineer | AWS Learner | Cybersecurity Enthusiast

GitHub: https://github.com/pentestfail15-hash

LinkedIn: https://www.linkedin.com/in/raj-kumar-1a3b493b1

---

## License

This project is created for educational purposes and hands-on AWS learning.
