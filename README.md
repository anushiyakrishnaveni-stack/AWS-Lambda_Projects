# AWS-Lambda_Projects

**AWS Lambda Mastery: Hands-on Lab Series**

This repository contains a comprehensive, step-by-step laboratory series focused on AWS Lambda. The curriculum transitions from basic serverless concepts to advanced architectural patterns including VPC networking, automated resource management, and concurrency optimization.

**📋 Repository Overview**

Each folder in this repository corresponds to a specific lab. The labs are designed to be executed sequentially, as they often build upon resources (IAM roles, VPCs, and functions) created in previous steps.

**Environment Requirements:**

**Region:** US East (N. Virginia) us-east-1.

**Account:** AWS Free Tier eligible (be sure to follow the "Clean Up" steps in each lab to avoid charges).

**Runtime:** Python 3.12.

**📂 Lab Details**

**Lab 1: Introduction to Lambda**

**Objective:** Establish a foundation in serverless computing and the AWS Lambda lifecycle.

**Key Tasks:** * Deploying a function using the "Hello World" Python blueprint.

Understanding the "Scale-on-Demand" nature of Lambda.

Configuring basic IAM execution roles.

Key Takeaway: Understanding the difference between "Cold Starts" and "Warm Starts" and how Lambda scales seamlessly with incoming requests.

**Lab 2: The Lambda Console & Management**

**Objective:** Master the AWS Management Console for Lambda and version control.

**Key Tasks:** * Managing the 75GB code storage limit.

Using the built-in Code Editor and the "Deploy" workflow.

Creating Shareable vs. Private test events.

Publishing Versions and understanding unique ARNs for immutable code states.

**Lab 3: Monitoring & Troubleshooting**

**Objective:** Use Amazon CloudWatch to gain visibility into function health and performance.

**Key Tasks:** * Analyzing core metrics: Invocations, Duration, Throttles, and Concurrent Executions.

Configuring Log Retention policies to manage costs.

Running complex queries using CloudWatch Logs Insights.

Exploring advanced tools like Lambda Insights and CodeGuru Profiler.

**Lab 4: Automation with IAM, EC2, and EventBridge**

**Objective:** Build a practical automation tool that interacts with other AWS services.

**Key Tasks:** * Writing Python (Boto3) code to automate EBS Snapshots.

Creating custom IAM inline policies for granular resource access.

Scheduling triggers using Amazon EventBridge (Cron-like expressions).

**Architecture:** EventBridge → Lambda → EC2 API → EBS Snapshot.

**Lab 5: Networking: Lambda Functions and VPCs**

**Objective:** Securely connect Lambda functions to private resources within a Virtual Private Cloud (VPC).

**Key Tasks:** * Troubleshooting "Time Out" errors when accessing private IP addresses.

Configuring Elastic Network Interfaces (ENI) within subnets.

Aligning Security Groups to allow communication between Lambda and EC2.

**Key Takeaway:** Lambda functions do not reside "inside" your VPC by default; they require specific ENI configuration to access private resources.

**Lab 6: Scaling with Reserved & Provisioned Concurrency**

**Objective:** Manage scaling limits and eliminate latency for critical applications.

**Key Tasks:** * Setting Reserved Concurrency to guarantee capacity and prevent "Noisy Neighbor" issues in an account.

Configuring Provisioned Concurrency for specific versions to eliminate cold starts.

**Key Takeaway:** Reserved Concurrency acts as a limit/guarantee, while Provisioned Concurrency keeps execution environments "pre-warmed" and ready.

**🛠️ Tech Stack**

Cloud Provider: Amazon Web Services (AWS)

Language: Python 3.x

SDK: Boto3 (AWS SDK for Python)

Services: Lambda, IAM, EC2, CloudWatch, EventBridge, VPC.

**⚠️ Cleanup**

To avoid unexpected AWS billing:

Delete the EventBridge triggers created in Lab 4.

Delete the EBS Snapshots created in Lab 4.

Terminate the EC2 instances from Lab 4 & 5.

Delete the Lambda functions (Training, PingTest, EC2Snapshots).
