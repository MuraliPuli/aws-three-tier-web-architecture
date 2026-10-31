
# Application Load Balancer Architecture

## Application Load Balancer (ALB)

An Application Load Balancer operates at Layer 7 (HTTP/HTTPS)
and distributes incoming application traffic across
registered targets.

## Architecture

- Load Balancer: Application Load Balancer
- Scheme: Internet-facing
- Placement: Public Subnets
- Availability Zones: Two
- Target Type: EC2 Instances
- Target Group: Application EC2 Instances

## Traffic Flow

1. Users send HTTP/HTTPS requests.
2. Traffic reaches the Application Load Balancer.
3. ALB forwards requests to healthy EC2 targets.
4. EC2 instances process application requests.
5. The application communicates with Amazon RDS when required.

## Health Checks

ALB periodically checks registered targets using configured
health check settings.

Unhealthy targets are removed from normal traffic routing
until they become healthy again.

## Benefits

- Distributes incoming application traffic.
- Supports multiple application instances.
- Performs health checks.
- Supports HTTPS termination.
- Improves application availability.
