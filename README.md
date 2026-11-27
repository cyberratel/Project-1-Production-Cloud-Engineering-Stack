###Production workflow order

### **1.1 Install and configure development tools**

1. Install Python.
2. Install VS Code.
3. Install Git.
4. Install Docker Desktop.
5. Install Terraform.
6. Install AWS CLI.
7. Configure AWS CLI.
8. Verify AWS CLI authentication.
9. Configure Git.
10. Create a GitHub account/repository connection in VS Code.
11. Verify Docker is running.
12. Verify Terraform installation.
13. Verify Python installation.
14. Verify GitHub connectivity.

### **1.2 Develop the Python application**

1. Create project directory.
2. Create Python application.
3. Create application requirements file.
4. Configure Python application.
5. Configure application environment variables.
6. Configure application health-check endpoint.
7. Configure application logging.
8. Configure application error handling.
9. Configure application database integration code.
10. Configure application Secrets Manager integration code.
11. Configure application persistent storage integration code.
12. Test application functionality locally.

### **1.3 Containerize the application**

1. Create Dockerfile.
2. Configure Docker image dependencies.
3. Configure Docker application startup command.
4. Build Docker image.
5. Run Docker container locally.
6. Test application inside Docker.
7. Verify application health-check endpoint.
8. Verify application logging.
9. Test container restart.
10. Verify application functionality.
11. Prepare application configuration for EC2, ECS and EKS deployments.

### **1.4 Prepare project repository**

1. Create GitHub repository.
2. Create project directory structure.
3. Initialize Git repository.
4. Create `.gitignore`.
5. Create README.md.
6. Add application files.
7. Add Dockerfile.
8. Add requirements file.
9. Commit project files.
10. Push project to GitHub.

## **PHASE 2 — Terraform Foundation and Infrastructure Deployment Preparation**

Before creating AWS infrastructure, prepare Terraform and its state management.

### **2.1 Configure Terraform**

1. Create Terraform project directory.
2. Create Terraform project structure.
3. Configure Terraform version requirements.
4. Configure AWS provider.
5. Configure AWS region.
6. Configure Terraform variables.
7. Configure Terraform outputs.
8. Configure Terraform resource naming.
9. Configure Terraform environment variables.
10. Configure Terraform state storage.

### **2.2 Bootstrap Terraform remote state**

The remote state backend must be prepared before using it for the main infrastructure deployment.

1. Create S3 bucket for Terraform state.
2. Enable S3 bucket versioning.
3. Configure S3 bucket encryption.
4. Configure S3 bucket access restrictions.
5. Configure Terraform state locking using S3 lockfiles.
6. Configure Terraform backend.
7. Initialize Terraform.
8. Verify remote state storage.

### **2.3 Configure Terraform workflow**

1. Configure Terraform initialization.
2. Configure Terraform formatting.
3. Configure Terraform validation.
4. Configure Terraform plan.
5. Configure Terraform apply.
6. Configure Terraform destroy.
7. Test Terraform initialization.
8. Test Terraform validation.
9. Test Terraform plan.
10. Verify Terraform state management.

## **PHASE 3 — GitHub Actions and CI/CD Authentication**

Prepare automated infrastructure deployment before starting the main infrastructure deployment.

### **3.1 Configure deployment authentication**

1. Create IAM deployment role for CI/CD.
2. Configure GitHub Actions OIDC identity provider.
3. Configure IAM trust policy.
4. Configure GitHub repository restrictions in the trust policy.
5. Configure IAM permissions for Terraform deployment.
6. Configure permissions for required AWS services.
7. Verify GitHub Actions OIDC authentication.

### **3.2 Create GitHub Actions workflow**

1. Create GitHub Actions workflow directory.
2. Create CI/CD workflow file.
3. Configure workflow triggers.
4. Configure GitHub Actions permissions.
5. Configure OIDC authentication.
6. Configure AWS credentials.
7. Configure Terraform initialization.
8. Configure Terraform formatting checks.
9. Configure Terraform validation.
10. Configure Terraform plan.
11. Configure Terraform apply workflow.
12. Configure deployment authentication through GitHub Actions OIDC.

### **3.3 Test CI/CD**

1. Push workflow files to GitHub.
2. Trigger GitHub Actions workflow.
3. Verify GitHub Actions authentication.
4. Verify Terraform initialization.
5. Verify Terraform validation.
6. Verify Terraform plan.
7. Test infrastructure deployment.
8. Verify successful infrastructure deployment.

## **PHASE 4 — AWS Networking and VPC Infrastructure**

Now begin building the actual AWS production environment.

### **4.1 Create VPC infrastructure**

1. Create VPC.
2. Configure VPC CIDR block.
3. Enable VPC DNS support.
4. Enable VPC DNS hostnames.
5. Create public subnets.
6. Create private application subnets.
7. Create private database subnets.
8. Distribute subnets across Availability Zones.

### **4.2 Configure internet connectivity**

1. Create Internet Gateway.
2. Attach Internet Gateway to VPC.
3. Create public route tables.
4. Configure public Internet Gateway routes.
5. Associate public subnets with route tables.
6. Create NAT Gateway.
7. Allocate Elastic IP for NAT Gateway.
8. Create private application route tables.
9. Configure private application outbound routes.
10. Associate private application subnets with route tables.
11. Create database route tables.
12. Associate private database subnets with route tables.
13. Verify subnet routing.

### **4.3 Configure network security**

1. Create application security groups.
2. Create database security groups.
3. Create EFS security group.
4. Create ALB security group.
5. Create VPC endpoint security group.
6. Configure inbound security group rules.
7. Configure outbound security group rules.
8. Restrict RDS access to application security groups.
9. Restrict EFS access to application security groups.
10. Verify network security rules.

### **4.4 Configure VPC Endpoints**

Create the private AWS service connectivity required by the production environment.

1. Create S3 Gateway VPC Endpoint.
2. Associate S3 endpoint with required route tables.
3. Create ECR API VPC Endpoint.
4. Create ECR Docker VPC Endpoint.
5. Create Secrets Manager VPC Endpoint.
6. Create CloudWatch Logs VPC Endpoint.
7. Create Systems Manager VPC Endpoint.
8. Create required Systems Manager messaging endpoints.
9. Configure VPC endpoint security groups.
10. Configure VPC endpoint policies.
11. Verify private connectivity to AWS services.

## **PHASE 5 — IAM Security, Storage, Database and Container Registry**

This phase prepares the shared infrastructure that all three deployment environments will use.

### **5.1 Configure foundational IAM permissions**

1. Create EC2 IAM role.
2. Configure EC2 IAM policies.
3. Create EC2 instance profile.
4. Configure EC2 permissions for Systems Manager.
5. Configure EC2 permissions for ECR.
6. Configure EC2 permissions for Secrets Manager.
7. Configure EC2 permissions for CloudWatch.
8. Configure least-privilege application permissions.

### **5.2 Create shared EFS storage**

EFS must be ready before deploying applications that depend on shared persistent storage.

1. Create EFS filesystem.
2. Configure EFS encryption at rest.
3. Create EFS mount targets.
4. Configure EFS security group.
5. Create EFS access point if required.
6. Configure EFS access point permissions.
7. Configure EFS directory permissions.
8. Verify EFS networking.
9. Verify EFS mount target availability.
10. Verify shared storage access.

### **5.3 Create RDS database infrastructure**

1. Create RDS subnet group.
2. Configure RDS security group rules.
3. Configure database engine.
4. Configure database instance specifications.
5. Configure database storage.
6. Configure database encryption.
7. Configure database backup settings.
8. Create RDS instance.
9. Configure database.
10. Verify RDS provisioning.
11. Verify database availability.
12. Verify private database connectivity.

### **5.4 Configure Secrets Manager**

1. Create Secrets Manager secret.
2. Generate or configure RDS credentials.
3. Store RDS credentials in Secrets Manager.
4. Configure secret encryption.
5. Configure EC2 IAM permissions for Secrets Manager.
6. Configure private Secrets Manager VPC Endpoint.
7. Configure secret access policies.
8. Verify private Secrets Manager access.
9. Verify application IAM access to secrets.

### **5.5 Create EBS storage**

Prepare the additional block storage required by the EC2 deployment.

1. Create additional EBS volume.
2. Configure EBS volume type.
3. Configure EBS encryption.
4. Configure EBS availability zone.
5. Verify EBS volume provisioning.

### **5.6 Create Amazon ECR container registry**

1. Create ECR repository.
2. Configure ECR image scanning.
3. Configure ECR encryption.
4. Configure ECR lifecycle policy.
5. Configure IAM permissions for ECR.
6. Authenticate Docker to ECR.
7. Tag Docker image.
8. Push Docker image to ECR.
9. Verify ECR image.
10. Configure ECR access through VPC Endpoints.
11. Test ECR access through VPC Endpoints.

## **PHASE 6 — Domain, SSL/TLS and Application Load Balancer Infrastructure**

Prepare the application entry point before deploying the production workloads.

### **6.1 Configure Route 53**

1. Create Route 53 hosted zone.
2. Configure domain name servers at the domain registrar.
3. Verify hosted zone delegation.
4. Prepare DNS records for EC2.
5. Prepare DNS records for ECS.
6. Prepare DNS records for EKS.

### **6.2 Configure SSL/TLS**

1. Request ACM SSL/TLS certificate.
2. Configure certificate domain names.
3. Create ACM DNS validation records.
4. Validate ACM certificate.
5. Verify certificate issuance.

### **6.3 Create Application Load Balancer**

1. Create ALB.
2. Configure ALB scheme.
3. Configure ALB networking.
4. Select public subnets.
5. Configure ALB security group.
6. Create EC2 Target Group.
7. Configure EC2 Target Group health checks.
8. Create ALB HTTP listener.
9. Create ALB HTTPS listener.
10. Attach ACM certificate.
11. Configure HTTP-to-HTTPS redirect.
12. Verify ALB configuration.

### **6.4 Prepare application traffic routing**

1. Configure EC2 application routing.
2. Prepare ECS application routing.
3. Prepare EKS ingress/load-balancer integration.
4. Configure listener rules.
5. Configure host-based routing.
6. Verify ALB listener configuration.
7. Verify Target Group health-check configuration.

*Note: ECS will use an IP-type Target Group. EC2 will use an instance-type Target Group. EKS can use the AWS Load Balancer Controller to provision an ALB; sharing an ALB with other environments requires deliberate IngressGroup configuration.*

## **PHASE 7 — Initial EC2 Instance and Application Deployment**

Now that networking, IAM, storage, database, secrets, container registry and load balancing are ready, build the initial EC2 application environment.

### **7.1 Create initial EC2 instance**

1. Create initial EC2 instance.
2. Select EC2 instance type.
3. Select AMI.
4. Configure private subnet networking.
5. Configure EC2 security group.
6. Attach EC2 IAM instance profile.
7. Configure EC2 User Data.
8. Configure EBS root volume.
9. Attach additional EBS volume.
10. Verify EC2 instance provisioning.

### **7.2 Configure EC2 operating environment**

1. Configure EC2 access through Systems Manager.
2. Verify EC2 access through SSM Session Manager.
3. Update operating system packages.
4. Install Docker.
5. Install Python.
6. Configure Docker service.
7. Configure Docker to start on boot.
8. Format additional EBS volume.
9. Create EBS mount directory.
10. Mount EBS volume.
11. Configure persistent EBS mounting.
12. Verify EBS mount.
13. Install EFS mount utilities.
14. Create EFS mount directory.
15. Configure EFS mounting.
16. Configure EFS permissions.
17. Configure EFS boot-time mounting.
18. Verify EFS mount.
19. Verify EBS read/write.
20. Verify EFS read/write.

### **7.3 Deploy initial Python application**

1. Authenticate EC2 to Amazon ECR.
2. Pull Docker image from ECR.
3. Configure application environment variables.
4. Configure Docker bind mount for EFS.
5. Configure application access to additional EBS.
6. Configure application access to RDS.
7. Configure application access to Secrets Manager.
8. Configure application startup.
9. Configure Docker container restart policy.
10. Configure application startup on reboot.
11. Start application container.
12. Verify application health-check endpoint.
13. Test application.
14. Test Python-to-RDS connection.
15. Test Secrets Manager access.
16. Test EFS read/write.
17. Test EBS read/write.
18. Verify application logging.
19. Verify EC2 application deployment.

### **7.4 Configure EC2 Application Load Balancer integration**

1. Register initial EC2 instance with EC2 Target Group.
2. Verify EC2 target registration.
3. Verify Target Group health checks.
4. Configure ALB routing to EC2 application.
5. Test ALB traffic.
6. Verify application availability through ALB.

### **7.5 Prepare EC2 Amazon Machine Image**

1. Finalize initial EC2 configuration.
2. Verify application files.
3. Verify Docker configuration.
4. Verify EBS configuration.
5. Verify EFS boot-time mount configuration.
6. Verify application startup configuration.
7. Create AMI.
8. Verify AMI.
9. Verify AMI and EBS snapshot mappings.

### **7.6 Create EC2 Launch Template**

1. Create Launch Template.
2. Configure AMI.
3. Configure instance type.
4. Configure private subnet networking.
5. Configure EC2 security group.
6. Configure IAM instance profile.
7. Configure EBS block device mappings.
8. Configure Launch Template User Data.
9. Configure EFS mounting in User Data.
10. Configure application startup.
11. Configure instance monitoring.
12. Verify Launch Template configuration.

### **7.7 Create EC2 Auto Scaling Group**

1. Create Auto Scaling Group.
2. Configure private application subnets.
3. Attach EC2 ALB Target Group.
4. Configure desired capacity.
5. Configure minimum capacity.
6. Configure maximum capacity.
7. Configure health checks.
8. Create scaling policies.
9. Create CloudWatch scaling alarms.
10. Verify Auto Scaling configuration.

### **7.8 Test EC2 production deployment**

1. Test Auto Scaling manual scale-out.
2. Verify new EC2 instances launch from AMI.
3. Verify Docker and Python on new EC2 instances.
4. Verify EBS attachment on new EC2 instances.
5. Verify automatic EFS mounting.
6. Verify application startup.
7. Verify ALB target registration.
8. Verify Target Group health checks.
9. Test Auto Scaling under load.
10. Test scale-in.
11. Test instance replacement.
12. Verify application availability.

## **PHASE 8 — Amazon ECS Fargate Production Deployment**

EC2 is now deployed. Move to the second production environment.

### **8.1 Configure ECS IAM and infrastructure**

1. Create ECS cluster.
2. Configure ECS cluster networking.
3. Create ECS task execution IAM role.
4. Configure ECS task execution IAM policies.
5. Create ECS task IAM role.
6. Configure ECS task IAM policies.
7. Configure IAM permissions for ECR.
8. Configure IAM permissions for Secrets Manager.
9. Configure IAM permissions for CloudWatch.
10. Configure ECS security groups.
11. Configure private subnet deployment.
12. Configure ECS logging with CloudWatch.
13. Verify ECS cluster provisioning.

### **8.2 Configure ECS task definition**

1. Create ECS task definition.
2. Configure Fargate launch type.
3. Configure Docker image from ECR.
4. Configure CPU allocation.
5. Configure memory allocation.
6. Configure container port mappings.
7. Configure container environment variables.
8. Configure Secrets Manager integration.
9. Configure RDS connectivity.
10. Configure EFS volume integration.
11. Configure EFS mount points.
12. Configure container logging.
13. Configure container health checks.
14. Verify ECS task definition.

### **8.3 Deploy ECS application**

1. Create ECS service.
2. Configure ECS service networking.
3. Configure private application subnets.
4. Configure ECS security groups.
5. Configure desired task count.
6. Configure ECS deployment strategy.
7. Configure ECS service Auto Scaling.
8. Configure minimum capacity.
9. Configure maximum capacity.
10. Configure ECS scaling policies.
11. Configure ECS CloudWatch alarms.
12. Attach ECS service to ALB Target Group.
13. Verify ECS service deployment.
14. Verify ECS task health.
15. Verify ALB target registration.

### **8.4 Test ECS production deployment**

1. Verify ECS task deployment.
2. Verify ECS service health.
3. Test application availability through ALB.
4. Verify application connectivity to RDS.
5. Verify EFS read/write.
6. Verify Secrets Manager access.
7. Verify CloudWatch logging.
8. Test ECS scaling.
9. Test ECS scale-out.
10. Test ECS scale-in.
11. Test container replacement.
12. Test ECS deployment.
13. Test ECS deployment rollback.
14. Verify ECS recovery.
15. Verify CloudWatch logs, metrics and alarms.

## **PHASE 9 — Amazon EKS Kubernetes Production Deployment**

The third production environment is Amazon EKS.

### **9.1 Create EKS cluster infrastructure**

1. Create EKS cluster.
2. Configure EKS cluster networking.
3. Configure Kubernetes control plane access.
4. Configure private application subnets.
5. Configure cluster endpoint access.
6. Configure EKS security groups.
7. Configure EKS access management.
8. Configure Kubernetes IAM permissions.
9. Create EKS managed node groups.
10. Configure worker node instance types.
11. Configure worker node IAM roles.
12. Verify EKS cluster provisioning.
13. Verify worker node registration.
14. Verify cluster connectivity.

### **9.2 Configure EKS security and permissions**

1. Configure IAM Roles for Service Accounts (IRSA) or EKS Pod Identity.
2. Configure Kubernetes service accounts.
3. Configure pod-level IAM permissions.
4. Configure Secrets Manager access.
5. Configure Kubernetes RBAC.
6. Configure namespace permissions.
7. Configure service account permissions.
8. Verify secure application access.

### **9.3 Install Kubernetes infrastructure components**

1. Configure `kubectl`.
2. Install Helm.
3. Configure AWS Load Balancer Controller IAM permissions.
4. Install AWS Load Balancer Controller.
5. Configure EFS CSI driver.
6. Install EBS CSI driver.
7. Configure CloudWatch observability components.
8. Verify Kubernetes infrastructure components.
9. Verify CSI drivers.
10. Verify AWS Load Balancer Controller.

### **9.4 Prepare Kubernetes application environment**

1. Create Kubernetes namespace.
2. Create Kubernetes ConfigMaps.
3. Configure application environment variables.
4. Configure application Secrets Manager integration.
5. Configure Kubernetes service accounts.
6. Configure application IAM permissions.
7. Verify namespace configuration.
8. Verify application permissions.

### **9.5 Configure Kubernetes persistent storage**

1. Configure EFS storage integration.
2. Create EFS StorageClass.
3. Configure EFS persistent volumes.
4. Configure EFS persistent volume claims.
5. Configure EFS mount permissions.
6. Configure EBS CSI storage integration.
7. Create EBS StorageClass.
8. Configure EBS persistent volumes where required.
9. Configure EBS persistent volume claims where required.
10. Verify EFS persistent storage.
11. Verify EBS persistent storage.

### **9.6 Deploy Python application to EKS**

1. Create Kubernetes Deployment.
2. Configure Docker image from ECR.
3. Configure replica count.
4. Configure container resource requests.
5. Configure container resource limits.
6. Configure application environment variables.
7. Configure RDS connectivity.
8. Configure EFS volume integration.
9. Configure EBS volume integration where required.
10. Configure application Secrets Manager integration.
11. Configure application health probes.
12. Configure readiness probes.
13. Configure liveness probes.
14. Deploy application.
15. Verify pod health.
16. Verify application deployment.
17. Test Python-to-RDS connection.
18. Test EFS shared storage.
19. Test Secrets Manager access.
20. Verify application availability.

### **9.7 Configure Kubernetes application traffic routing**

1. Create Kubernetes Service.
2. Configure Service type.
3. Create Kubernetes Ingress.
4. Configure AWS Load Balancer Controller integration.
5. Configure ALB Ingress rules.
6. Configure HTTPS integration.
7. Configure application traffic routing.
8. Verify ingress configuration.
9. Verify ALB target registration.
10. Test application access through ALB.

### **9.8 Configure EKS scaling**

1. Configure Horizontal Pod Autoscaler (HPA).
2. Configure pod resource monitoring.
3. Configure Kubernetes scaling policies.
4. Configure cluster capacity scaling.
5. Install or configure Cluster Autoscaler or Karpenter.
6. Configure worker node scaling.
7. Test pod scale-out.
8. Test pod scale-in.
9. Test worker node scaling.
10. Verify application availability during scaling.

### **9.9 Test EKS production deployment**

1. Verify Kubernetes cluster health.
2. Verify worker node health.
3. Verify pod deployment.
4. Test pod replacement.
5. Test pod scaling.
6. Test worker node scaling.
7. Test Kubernetes deployment rollback.
8. Test RDS connectivity.
9. Test EFS shared storage.
10. Test Secrets Manager access.
11. Verify ingress and ALB traffic.
12. Verify CloudWatch logs.
13. Verify CloudWatch metrics.
14. Verify CloudWatch alarms.
15. Verify application availability.

## **PHASE 10 — Route 53, Domain Routing and HTTPS Production Configuration**

Now connect the three deployed environments to their respective domain names.

### **10.1 Configure production DNS records**

1. Create EC2 DNS record.
2. Point EC2 DNS record to ALB.
3. Create ECS DNS record.
4. Point ECS DNS record to ALB.
5. Create EKS DNS record.
6. Point EKS DNS record to its ALB or configured shared ALB.
7. Configure host-based routing rules.
8. Verify Route 53 DNS resolution.

### **10.2 Verify SSL/TLS configuration**

1. Verify ACM certificate.
2. Verify certificate domain coverage.
3. Verify HTTPS listener.
4. Verify HTTP-to-HTTPS redirect.
5. Verify HTTPS access to EC2.
6. Verify HTTPS access to ECS.
7. Verify HTTPS access to EKS.
8. Verify SSL/TLS certificate validity.

### **10.3 Test domain routing**

1. Test `ec2.example.com`.
2. Verify traffic reaches EC2 application.
3. Test `ecs.example.com`.
4. Verify traffic reaches ECS application.
5. Test `eks.example.com`.
6. Verify traffic reaches EKS application.
7. Verify ALB host-based routing.
8. Verify application availability through all domains.

## **PHASE 11 — AWS Security and Governance**

Now strengthen the complete production environment with centralized security, governance and auditing.

### **11.1 Configure AWS account governance**

1. Configure AWS Organizations.
2. Create separate production, development and security accounts.
3. Configure organizational units.
4. Configure Service Control Policies.
5. Configure account-level security policies.
6. Configure IAM Identity Center.
7. Configure centralized access management.

### **11.2 Configure IAM security**

1. Review existing IAM users and roles.
2. Review IAM policies.
3. Create and manage IAM policies.
4. Apply least-privilege access.
5. Review EC2 IAM permissions.
6. Review ECS task IAM permissions.
7. Review EKS pod IAM permissions.
8. Review GitHub Actions deployment permissions.
9. Configure IAM Access Analyzer.
10. Audit AWS account activity.

### **11.3 Configure security monitoring**

1. Configure CloudTrail.
2. Configure AWS Config.
3. Configure Amazon GuardDuty.
4. Configure AWS Security Hub.
5. Review AWS Trusted Advisor recommendations.
6. Configure security findings.
7. Investigate security findings.
8. Review unauthorized access attempts.
9. Review configuration compliance.
10. Verify security monitoring.

## **PHASE 12 — AWS Monitoring, Observability and Troubleshooting**

Configure centralized monitoring for EC2, ECS, EKS, RDS and the Python application.

### **12.1 Configure CloudWatch monitoring**

1. Configure CloudWatch metrics.
2. Create CloudWatch dashboards.
3. Create CloudWatch alarms.
4. Configure EC2 monitoring.
5. Configure EC2 system logs.
6. Monitor EC2 CPU usage.
7. Monitor EC2 memory usage.
8. Monitor EC2 disk usage.
9. Monitor RDS performance.
10. Monitor ECS workloads.
11. Monitor EKS workloads.
12. Monitor application logs.
13. Monitor application health.
14. Configure CloudWatch notifications and alerting.

### **12.2 Configure application observability**

1. Configure centralized application logging.
2. Configure application log groups.
3. Configure log retention.
4. Configure application performance monitoring.
5. Configure AWS X-Ray.
6. Configure application tracing.
7. Monitor application requests.
8. Monitor database performance.
9. Monitor application errors.
10. Monitor application response times.

### **12.3 Configure infrastructure monitoring**

1. Monitor EC2 Auto Scaling.
2. Monitor EC2 Target Group health.
3. Monitor ECS service health.
4. Monitor ECS task failures.
5. Monitor EKS cluster health.
6. Monitor Kubernetes pod health.
7. Monitor worker node health.
8. Monitor ALB traffic.
9. Monitor ALB Target Group health.
10. Monitor RDS availability.
11. Monitor EFS storage.
12. Monitor EBS volumes.

### **12.4 Perform production troubleshooting**

1. Investigate failed deployments.
2. Troubleshoot network connectivity.
3. Investigate application errors.
4. Investigate database connectivity failures.
5. Investigate Secrets Manager access failures.
6. Investigate EFS mounting failures.
7. Investigate EBS mounting failures.
8. Investigate container failures.
9. Investigate Kubernetes pod failures.
10. Identify infrastructure performance problems.
11. Investigate failed health checks.
12. Generate incident reports.

## **PHASE 13 — AWS Backup and Disaster Recovery**

Prepare the infrastructure to recover from failures, accidental deletion and data loss.

### **13.1 Configure AWS Backup**

1. Create AWS Backup vault.
2. Configure backup encryption.
3. Create AWS Backup plans.
4. Configure backup schedules.
5. Configure backup retention policies.
6. Configure resource assignments.
7. Verify AWS Backup configuration.

### **13.2 Configure database and storage backups**

1. Configure EBS snapshots.
2. Configure EBS backup policies.
3. Configure RDS automated backups.
4. Configure RDS snapshot backups.
5. Configure RDS backup retention.
6. Configure RDS Multi-AZ.
7. Configure EFS backups.
8. Configure S3 versioning.
9. Configure S3 replication.
10. Verify backup completion.

### **13.3 Configure disaster recovery**

1. Understand Recovery Point Objectives (RPO).
2. Understand Recovery Time Objectives (RTO).
3. Configure Route 53 health checks.
4. Configure Route 53 failover routing.
5. Understand AWS Elastic Disaster Recovery.
6. Configure recovery procedures.
7. Document backup procedures.
8. Document recovery procedures.

### **13.4 Perform disaster recovery testing**

1. Simulate infrastructure failure.
2. Restore EBS resources from snapshots.
3. Restore RDS from backups.
4. Restore EFS data.
5. Restore application infrastructure.
6. Verify database recovery.
7. Verify storage recovery.
8. Verify application recovery.
9. Test disaster recovery procedures.
10. Document recovery results.

## **PHASE 14 — Final Production Validation and Documentation**

This is the final stage. Verify that the same application works correctly across all three independent deployment environments.

### **14.1 EC2 production validation**

1. Verify EC2 application deployment.
2. Verify EC2 Auto Scaling.
3. Verify EC2 application health.
4. Verify EC2 database connectivity.
5. Verify EC2 Secrets Manager access.
6. Verify EC2 EFS access.
7. Verify EC2 EBS access.
8. Verify EC2 ALB routing.
9. Verify EC2 domain and HTTPS.
10. Verify EC2 monitoring and alerts.

### **14.2 ECS production validation**

1. Verify ECS application deployment.
2. Verify ECS service health.
3. Verify ECS service Auto Scaling.
4. Verify ECS database connectivity.
5. Verify ECS Secrets Manager access.
6. Verify ECS EFS access.
7. Verify ECS ALB routing.
8. Verify ECS domain and HTTPS.
9. Verify ECS monitoring and alerts.
10. Verify ECS deployment rollback.

### **14.3 EKS production validation**

1. Verify EKS cluster health.
2. Verify Kubernetes application deployment.
3. Verify pod health.
4. Verify HPA scaling.
5. Verify worker node scaling.
6. Verify Kubernetes database connectivity.
7. Verify Secrets Manager access.
8. Verify EFS access.
9. Verify EBS persistent storage where required.
10. Verify Ingress and ALB routing.
11. Verify EKS domain and HTTPS.
12. Verify monitoring and alerts.
13. Verify Kubernetes deployment rollback.

### **14.4 Cross-environment application validation**

1. Verify the same Python application runs on EC2.
2. Verify the same Python application runs on ECS.
3. Verify the same Python application runs on EKS.
4. Verify all three environments use the intended RDS database.
5. Verify all three environments retrieve credentials securely.
6. Verify persistent storage functionality.
7. Verify application health checks.
8. Verify application logging.
9. Verify load balancing.
10. Verify application availability.
11. Verify scaling and recovery.
12. Verify production security.




## **The final workflow at a glance**

## **Production implementation sequence**

1. **Development environment and Python application**

   Python, Git, Docker, application development and local testing.
2. **Terraform foundation**

   Terraform, AWS CLI, remote state and infrastructure configuration.
3. **GitHub Actions and OIDC**

   Deployment IAM role and automated infrastructure deployment.
4. **VPC and networking**

   VPC, subnets, routing, NAT, security groups and VPC endpoints.
5. **Shared AWS infrastructure**

   IAM, EFS, RDS, Secrets Manager, EBS and ECR.
6. **Domain preparation and ALB**

   Route 53, ACM, HTTPS and application load balancing.
7. **EC2 production deployment**

   Initial EC2, Docker, EFS, EBS, AMI, Launch Template and Auto Scaling.
8. **ECS production deployment**

   ECS cluster, task definitions, Fargate, services and scaling.
9. **EKS production deployment**

   EKS cluster, worker nodes, Kubernetes, storage, Ingress and scaling.
10. **Domain and HTTPS activation**

    DNS records, host-based routing and production verification.
11. **Security and governance**

    Organizations, IAM, CloudTrail, Config, GuardDuty and Security Hub.
12. **Monitoring and troubleshooting**

    CloudWatch, X-Ray, logs, metrics, alarms and incident investigation.
13. **Backup and disaster recovery**

    AWS Backup, snapshots, replication, restoration and recovery testing.
14. **Final production validation**

    
