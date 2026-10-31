
# AWS IAM and Security Groups

## AWS IAM

AWS Identity and Access Management (IAM) controls access
to AWS services and resources.

## IAM Configuration

- IAM Roles for EC2 instances.
- Least-privilege permissions.
- IAM policies for required AWS services.
- No hardcoded AWS access keys in application code.

## Security Groups

Security Groups act as virtual firewalls controlling
inbound and outbound traffic.

## Security Group Design

### ALB Security Group
- Allows inbound HTTP (port 80) from permitted internet traffic.
- Allows HTTPS (port 443) from permitted internet traffic.
- Allows outbound application traffic to EC2 targets.

### Application EC2 Security Group
- Allows application traffic only from the ALB Security Group.
- Does not allow unrestricted public inbound access.

### RDS Security Group
- Allows database traffic only from the Application EC2 Security Group.
- Does not allow direct public database access.

## Security Benefits

- Controlled access between architecture layers.
- Reduced unnecessary network exposure.
- Better identity and permission management.
- Improved cloud security through least privilege.
