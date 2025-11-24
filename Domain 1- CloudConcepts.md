# AWS Cloud Practitioner — Domain 1 (Cloud Concepts)
A complete glossary-style **README.md** covering every **keyword, service, concept, and jargon** you must know for Domain 1 of the AWS Cloud Practitioner exam.  
Format: **Term → Explanation**  
This is meant to be your copy/paste crash-reference sheet.

---

## 📘 1. Cloud Computing Fundamentals

### **Cloud Computing**
On-demand delivery of compute, storage, databases, and other IT resources over the internet with pay-as-you-go pricing.

### **On-Demand Self-Service**
Ability to provision resources immediately without human approval from AWS.

### **Pay-As-You-Go Pricing**
You only pay for the resources actually consumed (compute, storage, data transfer).

### **Scalability**
Ability to increase resources based on demand.

### **Elasticity**
Automatic scaling up or down based on traffic patterns (Auto Scaling).

### **Agility**
Speed to deploy infrastructure and innovate quickly.

### **Fault Tolerance**
Ability to withstand failures without downtime, often using multiple AZs.

### **High Availability (HA)**
Keeping systems running with minimal downtime by using redundancy (multi-AZ).

---

## 📘 2. Six Advantages of Cloud Computing (Must Memorize)

### **Trade Capital Expense (CapEx) for Operational Expense (OpEx)**
Stop buying hardware upfront; instead pay for cloud usage monthly.

### **Benefit from Massive Economies of Scale**
AWS buys hardware at scale, lowering your resource costs.

### **Stop Guessing Capacity**
Scale on demand instead of over/under-provisioning.

### **Increase Speed and Agility**
Launch resources in minutes, not weeks.

### **Stop Spending Money Running Data Centers**
AWS handles physical infrastructure so you don’t have to.

### **Go Global in Minutes**
Deploy worldwide by choosing AWS Regions around the globe.

---

## 📘 3. Cloud Deployment Models

### **Public Cloud**
Cloud infrastructure available to many customers (AWS, Azure, GCP).

### **Private Cloud**
Cloud-like environment dedicated to a single organization (on-prem or hosted).

### **Hybrid Cloud**
Combines on-premises environments with cloud resources.

---

## 📘 4. Cloud Service Models

### **IaaS (Infrastructure as a Service)**
Provides virtualized compute/storage/networking.  
Examples: **EC2, EBS, VPC**

### **PaaS (Platform as a Service)**
Provides a platform for deploying applications without managing infrastructure.  
Examples: **Elastic Beanstalk, AWS Lambda (FaaS), Fargate**

### **SaaS (Software as a Service)**
Fully managed applications accessed over the internet.  
Examples: **Salesforce, Office 365, Zoom**

---

## 📘 5. AWS Global Infrastructure

### **AWS Region**
A geographic location containing multiple Availability Zones.  
Used for data residency, compliance, and latency.

### **Availability Zone (AZ)**
One or more physically separate data centers inside a Region with independent power, networking, and cooling.

### **Data Center**
The actual physical building with servers and infrastructure; grouped into AZs.

### **Edge Location**
Sites around the world used by CloudFront and Route 53 for low-latency content delivery.

### **Local Zones**
Extend AWS compute/storage closer to large population centers.

### **Wavelength Zones**
Edge computing infrastructure integrated with telecom 5G networks.

---

## 📘 6. Shared Responsibility Model

### **AWS Responsibility → “Security *of* the Cloud”**
AWS handles:
- Physical data centers
- Hardware
- Networking
- Virtualization
- Managed service infrastructure

### **Customer Responsibility → “Security *in* the Cloud”**
Customer handles:
- IAM policies
- Security groups / NACLs
- Data encryption
- OS patches on EC2
- Application code
- Network configuration

### **Shared Responsibility Examples**
- AWS manages the hardware behind S3; customers configure **S3 bucket policies**.
- AWS manages RDS infrastructure; customers manage **data, schema, and users**.

---

## 📘 7. Well-Architected Framework (High Level)

### **5 Pillars**
1. **Operational Excellence**  
2. **Security**  
3. **Reliability**  
4. **Performance Efficiency**  
5. **Cost Optimization**

---

## 📘 8. Cloud Economics

### **CapEx (Capital Expense)**
Large upfront cost to purchase hardware, data center space, etc.

### **OpEx (Operational Expense)**
Ongoing costs paid monthly (pay-as-you-go cloud billing).

### **AWS Pricing Calculator**
Estimate cost of AWS solutions before deployment.

### **AWS Cost Explorer**
View and analyze past AWS spending.

### **AWS Budgets**
Set budget alerts based on cost or usage thresholds.

### **AWS Cost & Usage Report**
Most detailed billing data; used for enterprise cost management.

---

## 📘 9. Data Transfer Basics

### **Data Transfer IN**
Usually free when sending data *into* AWS.

### **Data Transfer OUT**
Charges apply when data leaves AWS to the internet.

### **Same AZ Data Transfer**
Often free or reduced cost.

### **Inter-AZ Data Transfer**
Costs apply — important for architecture planning.

---

## 📘 10. Key Compute/Storage Terms (Domain 1 Level)

### **Amazon EC2**
Virtual servers in the cloud.

### **Amazon S3**
Object storage built for durability and scalability.

### **EBS (Elastic Block Store)**
Block storage for EC2 instances.

### **EFS (Elastic File System)**
Scalable shared file storage for Linux workloads.

### **Amazon RDS**
Managed relational database.

### **Amazon DynamoDB**
Managed NoSQL key-value database.

---

## 📘 11. Networking Basics (High Level)

### **VPC (Virtual Private Cloud)**
Isolated network environment in AWS.

### **Subnet**
Range of IP addresses in a VPC (public or private).

### **Security Group**
Virtual firewall controlling inbound/outbound traffic for AWS resources.

### **NACL (Network ACL)**
Subnet-level stateless firewall (optional layer of security).

### **Route 53**
AWS DNS service (scalable, global, supports latency routing).

---

## 📘 12. Content Delivery & Performance

### **Amazon CloudFront**
Global Content Delivery Network (CDN) using Edge Locations for low latency.

### **Global Accelerator**
Optimizes traffic routing over AWS global backbone to reduce latency.

---

## 📘 13. Backup & Durability Concepts

### **Durability**
Probability that data will not be lost.  
S3 durability = **99.999999999% (11 9’s)**.

### **Availability**
Uptime of a service (e.g., 99.99% uptime).

---

## 📘 14. Misc Domain 1 Terms

### **Elasticity vs Scalability**
- **Scalability** = ability to increase capacity.  
- **Elasticity** = ability to scale automatically based on demand.
  
### **Elasticity vs Scalability Scenario**
- **Scalability** = Hiring more employees when business grows.
- **Elasticity** = Hiring temporary workers who come in ONLY when customers show up.

  
### **Regions Are Isolated, AZs Are Connected**
Regions do not share control planes; AZs have low-latency links.

### **IAM (Identity and Access Management)**
Controls permissions and authentication (covered deeper in D

