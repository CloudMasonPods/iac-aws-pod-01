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
   - [ ] Launch an [RKE2](https://docs.rke2.io/install/quickstart) cluster in the private subnet using 3 small EC2 instances.
   

3. **Storage:**
   - [ ] Create an S3 bucket for storing static content and media files.
   - [ ] Set up RDS for the application's database.

4. **Security:**
   - [ ] Implement security groups and NACLs to control traffic flow.
   - [ ] Set up IAM roles and policies for resource access.
   - [ ] Configure GuardDuty for threat detection.

5. **CI/CD Pipeline:**
   - [ ] Use Terraform to automate the deployment of the entire infrastructure.
   - [ ] Integrate the infrastructure setup with a CI/CD pipeline using Atlantis or Terraform Cloud .

**Deliverables:**
   - [ ] Terraform scripts for setting up the VPC, subnets, EKS, EC2 instances, S3 bucket, and RDS.
   - [ ] Security policies and IAM configurations.
   - [ ] Documentation on the architecture and how each component is secured.
   - [ ] a 3 minute video showign your infrastructure setup and how it works

**Extra Credit:**
   - Implement a WAF to protect the web application.
   - Set up CloudWatch or Prometheus/grafana for monitoring and logging.
