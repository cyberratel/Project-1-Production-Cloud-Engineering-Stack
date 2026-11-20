## Implementation Workflow

### Phase 1: VPC and Network Foundation

1. Create a custom VPC using Terraform.
2. Create public and private subnets across two Availability Zones.
3. Create Internet Gateway and NAT Gateway.
4. Configure route tables and security groups.

### Phase 2: Compute and Load Balancing

5. Create EC2 instances in private subnets.
6. Create an Application Load Balancer in public subnets.
7. Connect the ALB to the EC2 instances.
8. Create an Auto Scaling Group across two Availability Zones.

### Phase 3: DNS and Domain Connectivity

9. Configure Route 53 record sets and connect the domain to the ALB.

### Phase 4: Advanced Network Connectivity

10. Create a second VPC and configure AWS PrivateLink connectivity.
11. Set up an AWS Site-to-Site VPN lab to connect an external network to the VPC.

### Phase 5: Infrastructure Automation and CI/CD

12. Use Terraform to manage and automate the infrastructure.
13. Configure GitHub Actions to validate and deploy the Terraform configuration.
