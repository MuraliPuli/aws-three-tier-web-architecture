
# AWS Three-Tier Application Workflow

## Architecture Workflow

### Step 1: User Request
A user accesses the application through a browser using
the Application Load Balancer endpoint.

### Step 2: Internet Gateway
Internet traffic reaches the public subnets through
the Internet Gateway and configured route tables.

### Step 3: Application Load Balancer
The ALB receives incoming HTTP/HTTPS requests and
forwards them to healthy registered EC2 targets.

### Step 4: Application Tier
EC2 instances in private application subnets process
the incoming requests.

The Auto Scaling Group manages application instance
capacity based on configured scaling policies.

### Step 5: Database Tier
When application data is required, the application
connects to Amazon RDS through private network connectivity.

### Step 6: Response
The application processes the database response and
returns the result through the Application Load Balancer
to the user's browser.

## Overall Architecture Benefits

- Separation of application layers.
- Better network security.
- Scalable application infrastructure.
- Health-based traffic distribution.
- Managed relational database.
- Multi-AZ architecture for improved availability.
