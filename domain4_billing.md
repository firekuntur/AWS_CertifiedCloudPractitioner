# AWS Cloud Practitioner — Domain 4: Billing, Pricing & Support  
**Complete Study Guide (CLF-C02)**  
Format: Definition • Explanation • Exam Tip • Scenario

---

# 📘 Task Statement 4.1 — AWS Pricing Models

---

## **On-Demand Instances**
**Definition:**  
Pay for compute capacity by the hour or second with no commitment.

**Explanation:**  
Best for unpredictable workloads, testing, or short-term tasks.

**Exam Tip:**  
If workload is **spiky or unknown**, choose On-Demand.

**Scenario:**  
A dev team runs a test server for a few hours → On-Demand fits best.

---

## **Reserved Instances (RIs)**
**Definition:**  
Commitment to 1 or 3 years of consistent instance usage for discounted pricing.

**Explanation:**  
- Standard RIs (biggest savings)  
- Convertible RIs (flexible instance families)  
- Scheduled RIs (specific time windows)

**Exam Tip:**  
RIs = **steady state workloads**  
Convertible RIs = **flexibility**

**Scenario:**  
A company runs databases 24/7 → RIs reduce cost significantly.

---

## **Reserved Instance Flexibility**
**Definition:**  
Ability for RIs to apply to different instance sizes within the same family.

**Explanation:**  
Example: An m5.large RI can apply to 2 × m5.medium.

**Exam Tip:**  
Convertible RIs → change instance type, OS, or tenancy.

**Scenario:**  
You switch from m5.large → m5.xlarge with Convertible RIs.

---

## **Reserved Instances in AWS Organizations**
**Definition:**  
RIs purchased in the management account apply across the organization.

**Explanation:**  
Unused RI discounts automatically float across accounts that match usage.

**Exam Tip:**  
RIs offer **shared discounts** inside Organizations.

**Scenario:**  
Account A buys RIs; Account B receives the discount automatically.

---

## **Spot Instances**
**Definition:**  
Deeply discounted compute capacity purchased from unused AWS inventory.

**Explanation:**  
Workloads can be interrupted with 2-minute notice.

**Exam Tip:**  
Spot = **cost savings** + **interruptible**.  
Never use Spot for critical workloads.

**Scenario:**  
Render farm or batch processing → Spot Instances.

---

## **Savings Plans**
**Definition:**  
Flexible pricing model committing to a usage amount per hour.

**Explanation:**  
Two types:
- **Compute Savings Plans** (most flexible)  
- **EC2 Instance Savings Plans** (specific instance family)

**Exam Tip:**  
Savings Plans = RIs but more flexible.

**Scenario:**  
You commit to $2
