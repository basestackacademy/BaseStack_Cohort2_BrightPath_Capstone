# Six-Week Course Concepts Checklist

Use this sheet to show where the project uses each week's ideas. Short answers are enough.

## Week 1 - Cloud Foundations
- [ ] Record the AWS Region selected by the instructor: ____________________
- [ ] In one sentence, explain why choosing a Region matters: ____________________
- [ ] Name one task that AWS is responsible for and one task the customer is responsible for: ____________________
- [ ] Explain the difference between a Region and an Availability Zone: ____________________

## Week 2 - IAM & Security
- [ ] Confirm you are signed in with the identity/role assigned by the instructor.
- [ ] Confirm MFA is enabled where you control the account. In a managed lab, do not change the instructor's identity settings.
- [ ] Explain why a broad administrator policy should not be attached to an ordinary application role: ____________________
- [ ] Open CloudTrail Event history and find a project event, such as `RunInstances` or `CreateBucket`. Save a screenshot.
- [ ] Explain in one sentence what AWS Organizations can help an organisation control: ____________________

## Week 3 - Networking (VPC)
- [ ] Create a VPC, one public subnet, an Internet Gateway, a route table, and a security group.
- [ ] Show the route `0.0.0.0/0` pointing to the Internet Gateway.
- [ ] Confirm the web security group allows HTTP (port 80) but has no inbound SSH (port 22) rule.
- [ ] Inspect the Network ACL without changing it.
- [ ] Explain why this one-public-server project does not need a NAT Gateway: ____________________

## Week 4 - Compute (EC2)
- [ ] Choose an Amazon Linux AMI and the smallest suitable instance type available in the training Region.
- [ ] Record why you selected the instance type and the price you checked: ____________________
- [ ] Confirm the website starts from EC2 User data; do not use a terminal.
- [ ] Explain when an Application Load Balancer and Auto Scaling Group would become useful: ____________________

## Week 5 - Storage (S3 & EBS)
- [ ] Create a private S3 backup bucket with Block Public Access left enabled.
- [ ] Confirm default encryption and enable versioning.
- [ ] Upload `index.html` through the S3 console and upload a second version after changing a sentence.
- [ ] Add a lifecycle rule for `archive/` objects to transition to S3 Standard-IA after 30 days. It will not transition during this short lab.
- [ ] Create a snapshot of the EC2 root EBS volume.
- [ ] Explain one case for EFS instead of EBS: ____________________

## Week 6 - Databases
- [ ] Complete `DATABASE_AND_SCALING_DECISIONS.md`.
- [ ] Explain why a basic informational website does not need a database yet: ____________________
