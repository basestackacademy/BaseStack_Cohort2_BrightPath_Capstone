# Six-Week Course Concepts Checklist

Use this sheet to show where the project uses each week's ideas. Short answers are enough.

## Week 1 - Cloud Foundations
- [*] Record the AWS Region selected by the instructor Ans: _eu-north-1a
- [*] In one sentence, explain why choosing a Region matters   Ans:For speed and latency
- [*] Name one task that AWS is responsible for and one task the customer is responsible for Ans: AWS:Handling the Cloud Security and USers:Handling security in the cloud.
- [*] Explain the difference between a Region and an Availability Zone Ans:Region is a gegraphical area while a Availability zone is a particular zone or centre in that geographical area.

## Week 2 - IAM & Security
- [*] Confirm you are signed in with the identity/role assigned by the instructor.
- [*] Confirm MFA is enabled where you control the account. In a managed lab, do not change the instructor's identity settings.
- [*] Explain why a broad administrator policy should not be attached to an ordinary application role Ans: It violates the principle of least privilege by granting excessive permissions that an application does not require.
- [*] Open CloudTrail Event history and find a project event, such as `RunInstances` or `CreateBucket`. Save a screenshot.
- [*] Explain in one sentence what AWS Organizations can help an organisation control Ans: AWS _manages Billing across all aws platforms while enforcing account-wide security and compliance guardrails using Service Control Policies (SCPs).

## Week 3 - Networking (VPC)
- [*] Create a VPC, one public subnet, an Internet Gateway, a route table, and a security group.
- [*] Show the route `0.0.0.0/0` pointing to the Internet Gateway.
- [*] Confirm the web sec urity group allows HTTP (port 80) but has no inbound SSH (port 22) rule.
- [*] Inspect the Network ACL without changing it.
- [*] Explain why this one-public-server project does not need a NAT Gateway Ans: It doesnt need a NAT Gateway clearly because the design uses only a single web server located inside a public subnet, which already has its own public IPv4 address and direct access to the Internet Gateway.

## Week 4 - Compute (EC2)
- [*] Choose an Amazon Linux AMI and the smallest suitable instance type available in the training Region.
- [*] Record why you selected the instance type and the price you checked Ans: _I selected t3.micro (2 vCPUs, 1 GiB RAM) because this informational, low-traffic static website does not require compute-intensive resources, and t3.micro is the modern burstable general-purpose standard in us-east-1.
- [*] Confirm the website starts from EC2 User data; do not use a terminal.
- [*] Explain when an Application Load Balancer and Auto Scaling Group would become useful Ans: _An ASG automatically launches or terminates EC2 instances across multiple Availability Zones based on demand metrics (such as CPU utilization during peak exam-prep seasons), while the ALB evenly distributes incoming user traffic across all healthy running instances to eliminate a single point of failure and prevent downtime.

## Week 5 - Storage (S3 & EBS)
- [*] Create a private S3 backup bucket with Block Public Access left enabled.
- [*] Confirm default encryption and enable versioning.
- [*] Upload `index.html` through the S3 console and upload a second version after changing a sentence.
- [*] Add a lifecycle rule for `archive/` objects to transition to S3 Standard-IA after 30 days. It will not transition during this short lab.
- [*] Create a snapshot of the EC2 root EBS volume.
- [*] Explain one case for EFS instead of EBS Ans: Amazon EFS is preferred over Amazon EBS when multiple EC2 instances need simultaneous, shared read-and-write access to the same centralized file system.

## Week 6 - Databases
- [*] Complete `DATABASE_AND_SCALING_DECISIONS.md`.
- [*] Explain why a basic informational website does not need a database yet Ans: _Because it is a static website serving pre-written, fixed content (like services, contact info, and business hours) that is identical for every visitor, meaning there is no dynamic user input, authentication, student accounts, payment records, or frequently changing data that requires querying, processing, or persistent relational storage.

