# 2-tier-Web-application-using-Ec2-ELB-ASG-and-Cloudwatch

---

**Scalable Web Application Infrastructure on AWS**

In this project, a robust and scalable web application infrastructure was designed and implemented on Amazon Web Services (AWS). The architecture encompasses a secure Virtual Private Cloud (VPC) configuration, a bastion host for secure access, an application server in a private subnet, a load balancer to distribute traffic, and an Auto Scaling Group (ASG) for dynamic scaling.

**Key Components:**

1. **VPC Configuration:** A Virtual Private Cloud (VPC) was meticulously configured to establish network isolation and security. This ensured that the application's components are shielded from external threats while adhering to best security practices.

2. **Bastion Host:** A bastion host was deployed in the public subnet, serving as an entry point for secure SSH access into the private instances. This adds an additional layer of security by limiting direct access to the private instances.

3. **Application Server:** An EC2 instance running Nginx was deployed within the private subnet. This application server is where the core web application resides, handling user requests, and processing application logic.

4. **Load Balancer:** An Application Load Balancer (ALB) was set up to distribute incoming traffic across the application servers. This ensures high availability and improved performance by balancing the load evenly.

5. **Auto Scaling Group (ASG):** An ASG was established with a dynamic simple scaling policy. The ASG dynamically adjusts the number of instances based on CPU utilization. When the CPU utilization surpasses 70%, the ASG adds a new instance to accommodate increased load. Conversely, when CPU utilization drops below 40%, an instance is removed, optimizing resource usage.

6. **CloudWatch Alarms:** CloudWatch alarms was configured to monitor the application server's CPU utilization. When the predefined thresholds were breached, these alarms triggered the ASG's scaling actions, promoting efficient resource allocation.

7. **Launch Template:** A launch template was created, using the AMI Image created of the application server. This enabled the rapid launch of identical instances to facilitate scaling.

8. **Testing and Validation:** The infrastructure's scalability has been validated by subjecting the application server to stress testing. The resulting increased CPU utilization triggered the CloudWatch alarm, which, in turn, led to the ASG dynamically adjusting the instance count, ensuring the application's responsiveness even during spikes in demand.

This project embodies a comprehensive and well-architected approach to building a scalable web application infrastructure. By thoughtfully integrating each component and leveraging AWS services for monitoring and automation, the result is a resilient and adaptable environment capable of meeting evolving application demands while maintaining a high level of performance and security.

--- 

