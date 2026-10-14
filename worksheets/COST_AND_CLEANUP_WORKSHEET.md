# Cost and Cleanup Worksheet

Complete this before launching the EC2 instance. Use the AWS Pricing Calculator or the pricing shown for your chosen Region. Do not assume that another student's estimate or free-tier eligibility applies to your account.

| Item | Your answer |
|---|---|
| AWS Region | ______________________________ |
| EC2 instance type selected | ______________________________ |
| Pricing source checked | ______________________________ |
| Estimated cost for the planned lab period | ______________________________ |
| EBS root volume size | ______________________________ |
| Are you deploying a NAT Gateway? Why/why not? | ______________________________ |
| Are you deploying a load balancer or Auto Scaling Group? Why/why not? | ______________________________ |
| Date and time you plan to clean up resources | ______________________________ |

## End-of-lab cleanup

- [ ] Terminate the EC2 instance.
- [ ] Delete the EBS snapshot after assessment.
- [ ] Empty the S3 bucket, including object versions, and delete the bucket.
- [ ] Delete the project security group, route table, Internet Gateway, subnet, and VPC in dependency order.
- [ ] Recheck the EC2, EBS, S3, and VPC consoles for remaining project resources.

**Cost reminder:** Terminating EC2 does not necessarily delete snapshots or S3 objects. Resources may still incur charges until they are deleted.
