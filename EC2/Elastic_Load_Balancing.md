# Elastic Load Balancing (ELB) Summary

## What is Elastic Load Balancing?
**Elastic Load Balancing (ELB)** is an AWS service that automatically distributes incoming application traffic across multiple resources, such as Amazon EC2 instances. It acts as a single point of contact for incoming traffic, ensuring better availability, fault tolerance, and scalability.

## Key Features
1. **Traffic Distribution**
   - Balances network traffic to ensure no single instance is overwhelmed.
   - Distributes incoming requests to healthy instances.

2. **Integration with Auto Scaling**
   - Works with **Amazon EC2 Auto Scaling** to dynamically add or remove instances based on traffic demand.
   - Ensures optimal resource utilization and cost efficiency.

3. **Load Balancer Types**
   - **Application Load Balancer (ALB)** – Best for HTTP/HTTPS traffic, supports path-based and host-based routing.
   - **Network Load Balancer (NLB)** – Designed for high-performance TCP/UDP traffic with ultra-low latency.
   - **Classic Load Balancer (CLB)** – Legacy option for simple load balancing across multiple EC2 instances.

4. **Health Checks**
   - Continuously monitors the health of target instances.
   - Automatically routes traffic only to healthy instances.

## Example Use Case
A website with fluctuating traffic can use an **Application Load Balancer (ALB)** to distribute incoming user requests across multiple EC2 instances. If traffic spikes, **Auto Scaling** adds more instances, and ELB ensures that requests are evenly distributed.

## Key Benefits
✅ **Improves availability** – Ensures application uptime even if some instances fail.  
⚡ **Enhances performance** – Distributes traffic efficiently to optimize resource usage.  
💰 **Cost savings** – Reduces the risk of over-provisioning by dynamically adjusting resources.  

---

## Final Thoughts
ELB is an essential component of high-availability and scalable AWS architectures. It ensures smooth traffic distribution, improves application resilience, and integrates seamlessly with **Auto Scaling** for optimal cloud performance. 🚀