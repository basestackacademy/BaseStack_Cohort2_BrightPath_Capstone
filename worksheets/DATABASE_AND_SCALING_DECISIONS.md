# Simple Database and Scaling Decisions

You do **not** need to create any of these extra services. Pick the service that best fits each situation and explain your choice in one or two sentences.

1. BrightPath later needs to store learners, lesson bookings, payment status and relationships between records. Which database type fits best: RDS/Aurora or DynamoDB? Why?

   My choice and reason: _________________________________________________

2. BrightPath adds a simple public timetable lookup with many reads and a key-based access pattern. Would DynamoDB be worth considering? Why?

   My answer: ____________________________________________________________

3. The website repeatedly reads the same timetable and should keep a short-lived copy to reduce repeated database reads. What role could ElastiCache play, and why should it not be the only copy of the data?

   My answer: ____________________________________________________________

4. If the relational database becomes important to business continuity, what does RDS Multi-AZ help with?

   My answer: ____________________________________________________________

5. Website visits grow and one EC2 instance is no longer enough. What roles would an Application Load Balancer and an Auto Scaling Group play?

   My answer: ____________________________________________________________

6. A private application server must download updates but must not accept inbound internet connections. What networking design might use a NAT Gateway, and why is that unnecessary for this project's public web server?

   My answer: ____________________________________________________________

7. A website has one server that needs its own boot disk, while several Linux servers need to share the same files. Which storage option fits each case: EBS or EFS?

   My answer: ____________________________________________________________

## Reminder
There can be more than one reasonable design. Marks are for a clear, sensible reason, not memorising a single sentence.
