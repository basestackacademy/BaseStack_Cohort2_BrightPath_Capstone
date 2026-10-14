# BaseStack Academy Cohort 2 - Simple Capstone

## BrightPath Tutors: A Small Business Website

Build and publish one simple informational website using the AWS Management Console and a browser. The project connects key concepts from Weeks 1-6 without deploying every AWS service.

## Start here
1. Open `STUDENT_PROJECT_GUIDE.pdf`.
2. Keep `STUDENT_PROJECT_GUIDE.md` open for searchable text.
3. Use `starter-materials/ec2-user-data.txt` only in the EC2 Launch Instance console's **User data** field. AWS runs it at first boot. Do not open a terminal or run it yourself.
4. Use `starter-materials/index.html` as the website backup uploaded through the S3 console.
5. Complete the worksheets and evidence checklist.

## What gets deployed
- One VPC, one public subnet, an Internet Gateway, one route table, and one web security group.
- One small EC2 instance with an EBS root volume, serving a simple website.
- One private S3 bucket for a backup copy, with encryption, versioning, and a lifecycle rule.
- One EBS snapshot and CloudTrail event-history evidence.

## Not required
No AWS CLI, terminal, CloudShell, SSH, Session Manager, database deployment, NAT Gateway, load balancer, Auto Scaling Group, or EFS deployment. Database and scaling services are covered in the short decision worksheet only.

## Important
Use the training account and Region approved by your instructor. Check cost and instance eligibility before launch. Delete the lab resources after assessment. Do not put real personal data, passwords, API keys, or private information on the sample site.
