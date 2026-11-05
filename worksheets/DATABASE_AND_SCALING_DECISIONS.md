# Simple Database and Scaling Decisions

You do **not** need to create any of these extra services. Pick the service that best fits each situation and explain your choice in one or two sentences.

1. BrightPath later needs to store learners, lesson bookings, payment status and relationships between records. Which database type fits best: RDS/Aurora or DynamoDB? Why?

   My choice and reason: RDS / Aurora. its use case involves a highly structured relational data with foreign-key relationships ( linking a specific student to multiple lesson bookings and matching payment transactions), requires ACID compliance to guarantee transactional consistency (preventing double-booking or missed payment records).

2. BrightPath adds a simple public timetable lookup with many reads and a key-based access pattern. Would DynamoDB be worth considering? Why?

   My answer: _Yes. DynamoDB is an excellent fit because key-value lookups (e.g., querying by CourseID or Date) match its primary access pattern, delivering consistent single-digit millisecond latency regardless of scale.

3. The website repeatedly reads the same timetable and should keep a short-lived copy to reduce repeated database reads. What role could ElastiCache play, and why should it not be the only copy of the data?

   My answer: ElastiCache is like an in-memory caching layer placed in front of the database to serve frequently requested timetable data directly from RAM at microsecond speeds, significantly reducing load and latency on the primary database.
4. If the relational database becomes important to business continuity, what does RDS Multi-AZ help with?

   My answer: RDS Multi-AZ provides high availability and automatic failover. AWS synchronously replicates data from the primary database instance to a dedicated standby replica in a different Availability Zone (AZ).
5. Website visits grow and one EC2 instance is no longer enough. What roles would an Application Load Balancer and an Auto Scaling Group play?

   My answer: __ASG monitors traffic metrics and automatically launches or terminates EC2 instances across multiple Availability Zones to handle demand spikes and maintain target capacity while, the Application Load Balancer (ALB) serves as the single public entry point, performing health checks.

6. A private application server must download updates but must not accept inbound internet connections. What networking design might use a NAT Gateway, and why is that unnecessary for this project's public web server?

   My answer: ___A NAT Gateway allows servers in a private subnet to download outbound updates without accepting inbound internet traffic, which is unnecessary here because our single server resides in a public subnet with direct internet access.

7. A website has one server that needs its own boot disk, while several Linux servers need to share the same files. Which storage option fits each case: EBS or EFS?

   My answer: __Amazon EBS provides a dedicated, low-latency boot disk for a single server, whereas Amazon EFS provides a shared network file system that multiple Linux servers can access simultaneously across Availability Zones.

## Reminder
There can be more than one reasonable design. Marks are for a clear, sensible reason, not memorising a single sentence.
