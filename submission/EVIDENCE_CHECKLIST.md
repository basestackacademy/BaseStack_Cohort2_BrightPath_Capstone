# Evidence Checklist

Use screenshots from the AWS Management Console and browser. Do not include passwords, access keys, account recovery details, or private information.

- [ ] VPC details showing the project CIDR.
- [ ] Public subnet details and its route table association.
- [ ] Route table showing `0.0.0.0/0` to the Internet Gateway.
- [ ] Security group inbound rules showing HTTP port 80 and no SSH port 22 rule.
- [ ] EC2 instance running, with instance type, AMI, and EBS volume visible.
- [ ] BrightPath Tutors website open in a browser using the instance public IPv4 address.
- [ ] Private S3 bucket with Block Public Access enabled and encryption shown.
- [ ] S3 versioning enabled and two versions of `index.html` visible.
- [ ] S3 lifecycle rule for prefix `archive/` visible.
- [ ] EBS snapshot completed.
- [ ] CloudTrail Event history with one project event.
- [ ] Completed Week concepts checklist and database/scaling worksheet.
- [ ] Cleanup proof: EC2 terminated, snapshot removed, bucket emptied/deleted, and networking resources removed.
