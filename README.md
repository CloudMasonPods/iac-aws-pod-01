# IAC-AWS-Pod

# Infrastructure Incubator 1 Sprint Requirements 

# Forking instrucitons(For Team Lead)
- [ ] Fork the repository to your own account
- [ ] Add the students as collaborators to the repository
- [ ] complete prerequisites 

# Prerequisites
- [ ] install terraform
- [ ] install AWS CLI 
- [ ] set up AWS account 

### Lab Scenario 1: Setting Up a Secure and Scalable Infrastructure

**Objective:**
Platform Engineers are tasked with building a secure and scalable infrastructure for a web application called “Comments.” This application is a distributed commenting system that aggregates data from comments rated 1 to 5 and provides data reports.
**Tasks:**

0. ** Terraform **
- [ ] Setup a Dynamodb for the terraform state file
- [ ] store state in an s3 bucket 

1. **VPC and Networking Setup:**
   - [ ] Create a VPC with public and private subnets.
   - [ ] Configure an Internet Gateway and a NAT Gateway.
   - [ ] Set up Route 53 for domain management.

2. **Compute Resources:**
   - Launch an EKS cluster in the private subnet.

3. **Storage:**
   - Create an S3 bucket for storing static content and media files.
   - Set up RDS for the application's database.

4. **Security:**
   - Implement security groups and NACLs to control traffic flow.
   - Set up IAM roles and policies for resource access.
   - Configure GuardDuty for threat detection.

5. **CI/CD Pipeline:**
   - Use Terraform to automate the deployment of the entire infrastructure.
   - Integrate the infrastructure setup with a CI/CD pipeline using Jenkins or GitLab CI.

**Deliverables:**
   - Terraform scripts for setting up the VPC, subnets, EKS, EC2 instances, S3 bucket, and RDS.
   - Security policies and IAM configurations.
   - Documentation on the architecture and how each component is secured.

**Extra Credit:**
   - Implement a WAF to protect the web application.
   - Set up CloudWatch for monitoring and logging.

### Lab Scenario 2: Building a Serverless Application

**Objective:**
Platform engineers need to build a serverless application for processing user uploads and generating reports.

**Tasks:**

1. **Serverless Framework Setup:**
   - Create a Lambda function for processing user uploads.
   - Set up API Gateway to trigger the Lambda function.
   - Use S3 for storing user uploads.

2. **Database and Storage:**
   - Use DynamoDB for storing metadata about the uploads.
   - Configure S3 for storing processed data.

3. **Event Handling:**
   - Set up S3 event notifications to trigger Lambda functions upon file uploads.
   - Use SNS for sending notifications about processing status.

4. **Security:**
   - Implement IAM roles and policies for Lambda and API Gateway.
   - Use AWS KMS for encrypting sensitive data.
   - Set up CloudTrail for auditing API calls.

5. **CI/CD Pipeline:**
   - Automate the deployment using Terraform and the Serverless framework.
   - Integrate the serverless application deployment with a CI/CD pipeline using AWS CodePipeline.

**Deliverables:**
   - Serverless framework configurations and Terraform scripts.
   - Security policies and IAM configurations.
   - Documentation on the serverless architecture and event handling.

**Extra Credit:**
   - Implement an SQS queue to handle retries and failures.
   - Set up CloudWatch Logs for monitoring Lambda executions.

### Lab Scenario 3: Implementing a Multi-Region Disaster Recovery Plan

**Objective:**
Platform engineers are responsible for setting up a multi-region disaster recovery plan for a mission-critical application.

**Tasks:**

1. **Primary Region Setup:**
   - Deploy the application infrastructure in the primary region, including VPC, subnets, EC2, RDS, and S3.

2. **Secondary Region Setup:**
   - Create a similar infrastructure setup in a secondary region for failover.
   - Use RDS Read Replicas for database synchronization.

3. **DNS and Traffic Management:**
   - Configure Route 53 for multi-region DNS failover.
   - Set up Route 53 health checks to monitor the application's availability.

4. **Replication and Synchronization:**
   - Use AWS S3 Cross-Region Replication for S3 buckets.
   - Implement database replication and failover mechanisms.

5. **Security:**
   - Ensure consistent security policies across both regions.
   - Set up IAM roles and policies for cross-region access.

6. **CI/CD Pipeline:**
   - Automate the deployment and failover setup using Terraform.
   - Integrate with a CI/CD pipeline to ensure consistent deployments in both regions.

**Deliverables:**
   - Terraform scripts for multi-region setup and failover configurations.
   - Security policies and IAM configurations.
   - Documentation on the disaster recovery plan and failover procedures.

**Extra Credit:**
   - Implement AWS Global Accelerator for improved global application performance.
   - Set up a CloudFormation StackSet for managing resources across multiple regions.
