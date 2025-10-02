# 3-Tier Highly Available AWS Cloud Architecture for Web Hosting
![image.png]  
This project covered the architectural design of a HA, scalable and fault tolerant 3-tier architecture. As simple as it looks, this architecture pre-provisions resources prior to actual usage, while having the flexibility of tearing down unhealthy or un-needed infrastructure components when not needed. Below is a detailed breakdown of this Three-tier architecture, along with a detailed explanation of the services in place: 
1. DNS services which are provided by Amazon Route 53. It provides DNS services to simplify domain management.
2. Edge caching with Amazon CloudFront. Edge caches high-volume content to decrease the latency to customers.
3. Edge security for Amazon CloudFront with AWS's Web Application Firewall. It filters malicious traffic, including cross site scripting (XSS) and SQL injection via customer-defined rules.
4. Load balancing with Elastic Load Balancing (ELB). This serves the role of enabling the spread of load across multiple Availability Zones and Amazon EC2 Auto Scaling groups for purposes of redundancy and decoupling of services.
5. DDoS protection with AWS Shield which safeguards the infrastructure against the most common network and transport layer DDoS attacks automatically.
6. Firewalls with security groups. Moves security to the instance level to provide a stateful, host-level firewall for both web and application servers.
7. Caching with Amazon ElastiCache. Works to provide caching services with Redis or Memcached to remove load from the app and database, and lower latency for frequent requests.
8. Managed database with Amazon Relational Database Service (Amazon RDS). Creates a highly available, multi-AZ database architecture.
9. Static storage and backups with Amazon S3. Provides simple HTTP-based object storage for backups and static assets like images and video.
