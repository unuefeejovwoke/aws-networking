# AWS Networking Setup

## Overview
This repository documents the process of setting up a fully functional VPC environment in AWS, including subnets across multiple availability zones, a NAT Gateway for outbound internet access from private subnets, and security mechanisms like security groups and NACLs.

## VPC and Subnet Configuration
- **VPC Creation**:
  - CIDR: 10.0.0.0/16
- **Subnets**:
  - Public Subnet: 10.0.1.0/24 (us-east-1a)
  - Private Subnet: 10.0.2.0/24 (us-east-1b)

## NAT Gateway Setup
- **Location**: Public Subnet (10.0.1.0/24)
- **Elastic IP**: Attached for internet connectivity.

## Security Configurations
- **Security Group**:
  - Allows inbound SSH and HTTP traffic.
- **Network ACLs**:
  - Custom rules to allow necessary traffic and block others as per the security policy.

## Testing and Validation
- **EC2 Instance**: Launched in the private subnet to test the connectivity through the NAT Gateway.
- **Connectivity Test**: Successfully connected to the internet without allowing inbound connections from outside the VPC.

## Screenshots and Logs
- Screenshots of the VPC, NAT Gateway setup, and security configurations are included in the `screenshots/` folder.

## Configuration Files
- JSON policies and configuration scripts can be found in the `config-files/` folder.

