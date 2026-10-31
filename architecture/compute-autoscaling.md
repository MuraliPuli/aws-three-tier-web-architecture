
# EC2 and Auto Scaling Architecture

## Amazon EC2

Amazon EC2 provides virtual servers to run the application
within private application subnets.

## EC2 Configuration

- Instance placement: Private Application Subnets
- Availability Zones: Two
- Application access: Through Application Load Balancer
- Public IP: Not required
- Security: Restricted using Security Groups

## Auto Scaling Group

An Auto Scaling Group manages the number of EC2 instances
based on configured scaling policies.

### Key Benefits

- Automatically increases instances when demand increases.
- Reduces instances when demand decreases.
- Replaces unhealthy instances.
- Supports application availability across multiple
  Availability Zones.

## Application Load Balancer Integration

The Application Load Balancer distributes incoming requests
to healthy EC2 instances registered in its target group.

Health checks help identify unhealthy application instances.
