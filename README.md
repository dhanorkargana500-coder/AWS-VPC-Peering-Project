# AWS VPC Peering Project

## Project Overview
This project demonstrates VPC Peering between two Amazon Virtual Private Clouds (VPCs) in the AWS Mumbai Region (`ap-south-1`).

The objective is to establish private network communication between EC2 instances deployed in separate VPCs using VPC Peering.

## Architecture

- **VPC A:** `10.10.0.0/16`
- **VPC B:** `10.20.0.0/16`
- **Public Subnet A:** `10.10.1.0/24`
- **Private Subnet A:** `10.10.2.0/24`
- **Private Subnet B:** `10.20.1.0/24`

### EC2 Instances

| Instance | Role | Private IP |
|---|---|---|
| Bastion Host | Secure SSH access | `10.10.1.10` |
| App-A | Private EC2 in VPC A | `10.10.2.10` |
| App-B | Private EC2 in VPC B | `10.20.1.10` |

## AWS Services Used

- Amazon VPC
- VPC Peering
- Amazon EC2
- Route Tables
- Security Groups
- Internet Gateway
- Amazon Linux 2023

## Implementation Steps

1. Created two separate VPCs.
2. Created public and private subnets.
3. Launched three EC2 instances.
4. Configured an Internet Gateway for public access to the Bastion Host.
5. Created and activated a VPC Peering connection.
6. Updated route tables to enable communication between VPCs.
7. Configured Security Groups to allow required SSH and ICMP traffic.
8. Connected to private EC2 instances through the Bastion Host.
9. Tested connectivity between App-A and App-B.
10. Performed a controlled connectivity failure test and restored the security rule.

## Connectivity Testing

- SSH access to private instances through the Bastion Host.
- ICMP ping testing between App-A and App-B.
- Verified successful communication.
- Temporarily removed an inbound ICMP rule to test connectivity failure.
- Restored the rule and verified connectivity again.

## Learning Outcomes

- Understanding VPC networking.
- Configuring VPC Peering.
- Managing route tables and Security Groups.
- Accessing private EC2 instances using a Bastion Host.
- Troubleshooting network connectivity.

## Project Details

**Project:** AWS VPC Peering  
**Organization:** EWB Edutech Private Limited (EWB Courses)  
**Internship Track:** AWS Cloud Computing  
**Region:** Asia Pacific (Mumbai) — `ap-south-1`

---

*This project was completed as part of an AWS Cloud Computing Internship.*
