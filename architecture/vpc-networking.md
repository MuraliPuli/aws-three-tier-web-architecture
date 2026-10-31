
# VPC and Networking

## Amazon VPC

Amazon VPC provides an isolated virtual network for hosting
AWS resources.

## Network Design

- VPC CIDR: 10.0.0.0/16
- Public Subnet AZ 1: 10.0.1.0/24
- Public Subnet AZ 2: 10.0.2.0/24
- Private Application Subnet AZ 1: 10.0.11.0/24
- Private Application Subnet AZ 2: 10.0.12.0/24
- Private Database Subnet AZ 1: 10.0.21.0/24
- Private Database Subnet AZ 2: 10.0.22.0/24

## Networking Components

### Internet Gateway
Allows resources in public subnets to communicate with the internet
when routing and security rules permit.

### Public Subnets
Host the Application Load Balancer.

### Private Application Subnets
Host EC2 application instances without direct public IP access.

### Private Database Subnets
Host Amazon RDS database resources without direct internet access.

### Route Tables
Control how network traffic moves between subnets and destinations.
