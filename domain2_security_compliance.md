# AWS Cloud Practitioner — Domain 2: Security & Compliance  
**Complete Study Guide — With Definitions, Explanations, Exam Tips, and Scenarios**  
Aligned 1:1 to the AWS CLF-C02 Official Exam Blueprint

---

# 📘 Domain 2.1 — AWS Shared Responsibility Model

## **Shared Responsibility Model**
**Definition:**  
A framework that outlines what security responsibilities AWS handles and what the customer must handle.

**Explanation:**  
AWS is responsible for the **security OF the cloud** (infrastructure).  
You (the customer) are responsible for the **security IN the cloud** (data, IAM, configurations).  
Responsibilities shift depending on service type (EC2, RDS, Lambda).

**Exam Tip:**  
Memorize this sentence:  
**AWS = OF the cloud. Customer = IN the cloud.**  
If the question mentions “infrastructure, hardware, data center,” → AWS.  
If it mentions “IAM, encryption settings, OS patching,” → Customer.

**Scenario:**  
You deploy an EC2 instance. AWS secures the physical host, but **you** must patch the OS and configure security groups.

---

## **AWS Responsibilities (Security OF the Cloud)**
**Definition:**  
What AWS fully manages for you.

**Explanation:**  
AWS handles:
- Data center physical security  
- Hardware (servers, storage, networking)  
- Virtualization layer  
- Managed service infrastructure  

**Exam Tip:**  
If the responsibility involves **physical hardware** or **global infrastructure**, it's ALWAYS AWS.

**Scenario:**  
A disk fails inside an AWS data center. AWS replaces it — you do nothing.

---

## **Customer Responsibilities (Security IN the Cloud)**
**Definition:**  
What the customer must manage/configure.

**Explanation:**  
Customer handles:
- IAM users, roles, policies  
- Security Groups, NACLs  
- OS updates on EC2  
- Data encryption choices  
- Networking configuration  
- Application code  
- Resource permissions  

**Exam Tip:**  
If the action touches **your data or your settings**, it’s your responsibility.

**Scenario:**  
You forget to block public access on an S3 bucket — this is YOUR responsibility.

---

## **Shared Responsibilities**
**Definition:**  
Parts of security where AWS provides tools but the customer chooses configuration.

**Explanation:**  
Examples:
- Patching for managed services (AWS patches RDS OS; you patch DB schema).  
- S3 durability provided by AWS; customer sets bucket policies and access.

**Exam Tip:**  
RDS is the classic shared responsibility example.

**Scenario:**  
AWS patches the RDS database engine; you must manage database users and tables.

---

## **How Responsibilities Shift by Service**
**Definition:**  
Managed services reduce customer responsibility.

**Explanation:**  
- **EC2:** You manage everything above the hypervisor (OS, patches, SGs).  
- **RDS:** AWS handles OS and DB engine; you handle data and access.  
- **Lambda:** AWS handles servers and runtime; you handle code and IAM.

**Exam Tip:**  
The more "managed" the service, the less YOU manage.

**Scenario:**  
With Lambda, you NEVER patch an OS — AWS handles it.

---

# 📘 Domain 2.2 — AWS Security, Governance & Compliance Concepts

---

## **AWS Compliance**
**Definition:**  
AWS maintains compliance programs (SOC, PCI, HIPAA, ISO) for its cloud infrastructure.

**Explanation:**  
Customers inherit these controls but must configure their own applications securely.
