
# Amazon RDS and Database Security

## Amazon RDS

Amazon Relational Database Service (RDS) is used to host
and manage the application's relational database.

## Database Architecture

- Database service: Amazon RDS
- Network placement: Private Database Subnets
- Availability: Multi-AZ deployment (reference design)
- Internet access: No direct public access
- Connectivity: Application Tier only

## Database Security

### Private Subnets
Database resources are placed in private subnets to prevent
direct public internet access.

### Security Groups
The database Security Group allows inbound database traffic
only from the Application Tier Security Group.

### Database Credentials
Database credentials should be stored securely and should
never be hardcoded in application source code.

### Multi-AZ
Multi-AZ deployment provides a standby database in another
Availability Zone for supported failover scenarios.

## Benefits

- Better database isolation.
- Restricted database connectivity.
- Managed database backups.
- Improved availability with Multi-AZ configuration.
