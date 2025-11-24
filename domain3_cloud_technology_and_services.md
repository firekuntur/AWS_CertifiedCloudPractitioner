# AWS Cloud Practitioner — Domain 3: Cloud Technology & Services  
**Complete Study Guide (CLF-C02)**  
Format: Definition • Explanation • Exam Tip • Scenario  

---

# 📘 Task Statement 3.1 — Deploying & Operating in the AWS Cloud

---

## **AWS Provisioning & Operating Methods**
**Definition:**  
Different ways to create, manage, automate, and operate AWS resources.

**Explanation:**  
You can interact with AWS in several ways:
- **AWS Management Console** (GUI)  
- **AWS CLI** (command line)  
- **AWS SDKs** (programmatic access using languages like Python, Java)  
- **AWS APIs**  
- **Infrastructure as Code (IaC)** tools (CloudFormation, CDK, Terraform)  

**Exam Tip:**  
If question mentions *“repeatable, consistent deployments”* → use IaC.  
If question mentions *“one-time, quick setup”* → AWS Console.

**Scenario:**  
A developer automates EC2 deployment using CloudFormation instead of manually configuring instances.

---

## **Ways to Access AWS Services**
**Definition:**  
Interfaces for interacting with AWS.

**Explanation:**  
- **Console** → best for beginners or manual tasks  
- **CLI** → for scripting, automation  
- **SDKs** → integrate AWS into applications  
- **API endpoints** → direct calls  
- **IaC** → fully automated infrastructure  

**Exam Tip:**  
SDK = programmatic integration.  
CLI = automation.  
Console = manual operations.

**Scenario:**  
A Python app uses the AWS SDK (boto3) to upload files to S3.

---

## **Cloud Deployment Models**
**Definition:**  
Different ways organizations deploy workloads.

**Explanation:**  
- **Cloud** → Fully hosted on AWS  
- **Hybrid Cloud** → Mix of AWS + on-premises  
- **On-Premises (Private Cloud)** → Physically controlled by company  

**Exam Tip:**  
Hybrid cloud shows up often → key phrase: *“on-prem + AWS”*.

**Scenario:**  
A company uses Direct Connect to link their on-prem DC to AWS → Hybrid.

---

## **One-Time vs Repeatable Processes**
**Definition:**  
Choosing between manual or automated operations.

**Explanation:**  
- **One-time:**  
  - Console-based setup  
  - Ad-hoc resources  

- **Repeatable:**  
  - IaC  
  - CLI scripts  
  - Version-controlled templates  

**Exam Tip:**  
Repeatability = IaC.  
Speed = console or CLI.

**Scenario:**  
A company creates 10 identical VPCs using CloudFormation templates.

---

---

# 📘 Task Statement 3.2 — AWS Global Infrastructure

---

## **AWS Regions**
**Definition:**  
Geographically distinct areas where AWS clusters data centers.

**Explanation:**  
Each Region contains multiple AZs and provides data residency options.

**Exam Tip:**  
Choose Region based on **latency, cost, service availability, and compliance**.

**Scenario:**  
A company must store data in the EU → choose `eu-central-1`.

---

## **Availability Zones (AZs)**
**Definition:**  
Physically separate data centers inside a Region.

**Explanation:**  
Each AZ has its own power, networking, and cooling, preventing single points of failure.

**Exam Tip:**  
High availability = deploy across **multiple AZs**.

**Scenario:**  
Deploying EC2 instances in 3 AZs ensures uptime during an AZ outage.

---

## **Edge Locations**
**Definition:**  
Global cache nodes used by CloudFront, Route 53, and Global Accelerator.

**Explanation:**  
Optimized for low-latency content delivery.

**Exam Tip:**  
Edge Location ≠ Region.  
Used for caching, not compute.

**Scenario:**  
CloudFront caches images at edge locations for fast load times.

---

## **Use Cases for Multiple Regions**
**Explanation:**  
Use multiple Regions for:
- Disaster Recovery  
- Business Continuity  
- Global low-latency apps  
- Data sovereignty  

**Exam Tip:**  
DR & low latency = multi-Region.

**Scenario:**  
A banking app mirrors data to another Region to meet compliance requirements.

---

---

# 📘 Task Statement 3.3 — AWS Compute Services

---

## **Amazon EC2**
**Definition:**  
Virtual servers in the cloud.

**Explanation:**  
Offers different instance types:
- **Compute Optimized (C5)**  
- **Memory Optimized (R5)**  
- **Storage Optimized (I3)**  
- **General Purpose (T-series, M-series)**  

**Exam Tip:**  
Compute-heavy tasks → C series  
Memory-heavy tasks → R series  
Storage-heavy tasks → I series

**Scenario:**  
Video rendering → C5  
In-memory DB → R5  
High IOPS DB → I3

---

## **Containers**
### **Amazon ECS**
**Definition:**  
AWS-managed container orchestration.

**Exam Tip:**  
If the question mentions “simple container management” → ECS.

### **Amazon EKS**
**Definition:**  
Managed Kubernetes service.

**Exam Tip:**  
If Kubernetes is explicitly needed → EKS.

### **AWS Fargate**
**Definition:**  
Serverless compute for ECS/EKS.

**Exam Tip:**  
“Run containers without managing servers” → Fargate.

**Scenario:**  
A microservices workload uses EKS with Fargate for serverless scaling.

---

## **Serverless Compute**
### **AWS Lambda**
**Definition:**  
Run code without provisioning servers.

**Exam Tip:**  
If billed per request or event-driven → Lambda.

### **Elasticity via Auto Scaling**
**Definition:**  
Automatically adjusts EC2 capacity.

**Exam Tip:**  
Elasticity = Auto Scaling.

**Scenario:**  
Auto Scaling adds EC2 instances during traffic spikes.

---

## **Load Balancers**
**Definition:**  
Distribute incoming traffic across multiple targets.

**Types:**
- **ALB** (Layer 7)  
- **NLB** (Layer 4)  
- **CLB** (legacy)  

**Exam Tip:**  
Multiple AZ high availability = Load Balancer + Auto Scaling.

**Scenario:**  
ALB routes HTTP traffic among many EC2 instances.

---

---

# 📘 Task Statement 3.4 — AWS Database Services

---

## **Relational Databases**
### **Amazon RDS**
**Definition:**  
Managed relational database (SQL Server, MySQL, PostgreSQL, etc.).

**Explanation:**  
AWS manages:
- OS  
- Patching  
- Backups  
- Multi-AZ  

Customer handles:
- Schema  
- Data  
- Users  

**Exam Tip:**  
For ease of management → choose RDS.

**Scenario:**  
A production database uses Multi-AZ RDS for high availability.

---

### **Amazon Aurora**
**Definition:**  
AWS-built relational database compatible with MySQL/PostgreSQL.

**Exam Tip:**  
High-performance, highly scalable → Aurora.

---

## **NoSQL Databases**
### **Amazon DynamoDB**
**Definition:**  
Fully managed NoSQL key-value and document database.

**Exam Tip:**  
Choose DynamoDB for **massive scale** or **millisecond latency**.

---

## **In-Memory Databases**
### **Amazon ElastiCache**
**Definition:**  
In-memory database supporting Redis/Memcached.

**Exam Tip:**  
Caching layer → ElastiCache.

---

## **Database Migration Tools**
### **AWS DMS**
**Definition:**  
Migrate/live replicate databases with minimal downtime.

### **AWS SCT**
**Definition:**  
Converts schema between engines (Oracle → Aurora).

**Exam Tip:**  
Schema conversion = SCT.  
Ongoing replication = DMS.

---

---

# 📘 Task Statement 3.5 — AWS Network Services

---

## **Amazon VPC**
**Definition:**  
Virtual network in AWS.

**Components:**  
- Subnets (public/private)  
- Route Tables  
- Internet Gateway  
- NAT Gateway  
- VPC Peering  
- VPC Endpoints  

**Exam Tip:**  
Subnets = IP ranges inside a VPC.

**Scenario:**  
Web servers in public subnet, databases in private subnet.

---

## **Security in VPC**
### **Security Groups**
- Instance-level  
- Stateful  

### **Network ACLs**
- Subnet-level  
- Stateless  

### **Amazon Inspector**
- Scans EC2 for vulnerabilities

**Exam Tip:**  
Stateless = NACL.

---

## **Route 53**
**Definition:**  
DNS service that performs:
- Domain registration  
- Routing policies  
- Health checks  

**Exam Tip:**  
Low-latency routing → Route 53 latency routing.

---

## **Network Connectivity Options**
### **AWS VPN**
Encrypted connection over the internet.

### **AWS Direct Connect**
Dedicated private fiber connection to AWS.

**Exam Tip:**  
Low latency + steady performance → Direct Connect.

---

---

# 📘 Task Statement 3.6 — AWS Storage Services

---

## **Object Storage**
### **Amazon S3**
**Definition:**  
Durable, scalable object storage.

**Use cases:**  
- Backups  
- Media hosting  
- Data lakes  

**Exam Tip:**  
Objects = “files with metadata.”

---

## **S3 Storage Classes**
- Standard  
- Intelligent Tiering  
- Standard-IA  
- One Zone-IA  
- Glacier  
- Glacier Deep Archive  

**Exam Tip:**  
Glacier = archival.  
One Zone-IA = cheap but not multi-AZ.

---

## **Block Storage**
### **EBS**
Durable block storage for EC2.

### **Instance Store**
Temporary storage physically attached to host.

**Exam Tip:**  
Delete-on-stop? → Instance Store.

---

## **File Storage**
### **EFS**
Managed NFS for Linux.

### **FSx**
High-performance Windows or Lustre file systems.

**Exam Tip:**  
Windows file share → FSx for Windows.

---

## **Cached File Systems**
### **AWS Storage Gateway**
Hybrid cloud storage bridging on-prem to S3.

**Scenario:**  
On-prem applications store files to AWS using File Gateway.

---

## **Lifecycle Policies**
Move objects to cheaper storage classes automatically.

**Scenario:**  
Move logs from S3 Standard → Glacier after 30 days.

---

## **AWS Backup**
Centralized backup service for AWS resources.

---

---

# 📘 Task Statement 3.7 — AI/ML & Analytics Services

---

## **AI/ML Services**
### **Amazon SageMaker**
Build, train, and deploy ML models.

### **Amazon Lex**
Conversational AI (chatbots).

### **Amazon Kendra**
Enterprise search engine.

**Exam Tip:**  
If question involves chatbots → Lex.  
Search engine → Kendra.  
ML model training → SageMaker.

---

## **Analytics Services**
### **Amazon Athena**
Query S3 data using SQL.

### **Amazon Kinesis**
Real-time streaming ingestion.

### **AWS Glue**
ETL (extract, transform, load) service.

### **Amazon QuickSight**
Business analytics dashboards.

**Exam Tip:**  
Real-time streaming → Kinesis.  
Query S3 → Athena.  
Dashboards → QuickSight.

---

---

# 📘 Task Statement 3.8 — Other In-Scope AWS Categories

---

## **Application Integration**
### **Amazon SNS**
Pub/sub notifications.

### **Amazon SQS**
Message queue service.

### **Amazon EventBridge**
Event bus connecting applications.

**Exam Tip:**  
SNS = push notifications  
SQS = queue & decouple  
EventBridge = event routing

---

## **Business Applications**
### **Amazon Connect**
Cloud contact center.

### **Amazon SES**
Email sending service.

---

## **Customer Enablement**
### **AWS Support Plans**
- Basic  
- Developer  
- Business  
- Enterprise  

---

## **Developer Tools**
### **CodeBuild**
Build code.

### **CodePipeline**
CI/CD automation.

### **X-Ray**
Application tracing.

**Exam Tip:**  
Trace microservices → X-Ray.

---

## **End-User Computing**
### **AppStream 2.0**
Stream desktop apps.

### **WorkSpaces**
Virtual desktops.

### **WorkSpaces Secure Browser**
Browser isolation service.

---

## **Frontend & Mobile**
### **AWS Amplify**
Deploy full-stack web/mobile apps.

### **AWS AppSync**
GraphQL API service.

---

## **IoT Services**
### **AWS IoT Core**
Connect and manage IoT devices.

---

# ✔ Domain 3 Study Guide Complete
This includes every line from the AWS CLF-C02 exam blueprint for Domain 3.

Let me know when you're ready for:
🔥 Domain 3 Practice Exam  
🔥 Domain 4 Study Guide  
🔥 A complete 4-domain exam cram PDF  
🔥 Flashcards for Domain 3  
