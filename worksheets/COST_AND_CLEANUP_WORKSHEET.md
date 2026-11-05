# Cost and Cleanup Worksheet

Complete this before launching the EC2 instance. Use the AWS Pricing Calculator or the pricing shown for your chosen Region. Do not assume that another student's estimate or free-tier eligibility applies to your account.

| Item | Your answer |
|---|---|
| AWS Region | __eu-north-1 (Europe - Stockholm)
| EC2 instance type selected | _t3.micro|
| Pricing source checked | AWS EC2 On-Demand Pricing / AWS Pricing Calculator |
| Estimated cost for the planned lab period | $0.17 – $0.29 total |
| EBS root volume size | 8 GiB (gp3 standard default) |
| Are you deploying a NAT Gateway? Why/why not? | NO. The NAT Gateway allows servers in a private subnet to download outbound updates without accepting inbound internet traffic, which is unnecessary here because our single server resides in a public subnet with direct internet access. |
| Are you deploying a load balancer or Auto Scaling Group? Why/why not? | NO. This is a single, low-traffic static website with no high-availability or multi-instance redundancy requirements, so a load balancer and Auto Scaling Group would introduce unnecessary architectural overhead and idle hourly costs. |
| Date and time you plan to clean up resources | 11/05/2026, 4:25 AM |

## End-of-lab cleanup

- [*] Terminate the EC2 instance.
- [*] Delete the EBS snapshot after assessment.
- [*] Empty the S3 bucket, including object versions, and delete the bucket.
- [*] Delete the project security group, route table, Internet Gateway, subnet, and VPC in dependency order.
- [*] Recheck the EC2, EBS, S3, and VPC consoles for remaining project resources.

**Cost reminder:** Terminating EC2 does not necessarily delete snapshots or S3 objects. Resources may still incur charges until they are deleted.
