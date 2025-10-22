![AWS Cloud Migration Case Study](https://img.shields.io/badge/Cloud%20Architecture-Hybrid%20%7C%20Full%20AWS%20Migration-orange?logo=amazon-aws&logoColor=white&style=for-the-badge)

# ☁️ Case Study: Cross Country Trains Cloud Migration Project

**🚀 Summary:**  
Analyzed and resolved **Cross Country Trains’ infrastructure challenges** including **double booking**, **peak-hour traffic spikes**, and **high on-prem maintenance costs**.  
Developed two scalable AWS-based architectures — **Full Cloud Migration** and **Hybrid Cloud (Burst Model)** — with **cost analysis, redundancy planning**, and a **final recommendation** using the **AWS Pricing Calculator** and real-world benchmarks.

---

![AWS](https://img.shields.io/badge/AWS-Architecture-orange?logo=amazon-aws&logoColor=white)
![Lambda](https://img.shields.io/badge/Compute-Lambda-yellow?logo=awslambda&logoColor=white)
![DynamoDB](https://img.shields.io/badge/Database-DynamoDB-blue?logo=amazondynamodb&logoColor=white)
![ElastiCache](https://img.shields.io/badge/Cache-ElastiCache-teal?logo=amazonaws&logoColor=white)
![SQS](https://img.shields.io/badge/Queue-SQS-purple?logo=amazonsqs&logoColor=white)
![Hybrid](https://img.shields.io/badge/Architecture-Hybrid%20%7C%20Serverless-success)
![Cost](https://img.shields.io/badge/Analysis-AWS%20Pricing%20Calculator-lightgrey)

---

### **🧩 What**
- Designed two architectures to address **scalability, latency, redundancy**, and **cost-efficiency**:
  - **Solution 1:** Full AWS Cloud Migration (Serverless Architecture)
  - **Solution 2:** Hybrid Cloud “Burst” Model (On-Prem + AWS)  
- Analyzed **double-booking prevention**, **peak-hour performance**, and **cost trade-offs** between models.  
- Provided a **five-year Total Cost of Ownership (TCO)** analysis comparing **On-Prem, Hybrid, and Full Cloud**.  
- Delivered detailed service diagrams, function mappings, and **AWS Pricing Calculator estimates**.  

---

## **⚙️ How**

**Tech Stack:**  
**AWS Services:** API Gateway • Lambda • SQS • DynamoDB • ElastiCache • EC2 • Route 53 • ELB • Auto Scaling • DMS  
**Core Concepts:** Scalability • Redundancy • Cost Optimization • Availability • Disaster Recovery  

**Solution 1 – Full Cloud (Serverless Architecture)**  
- **API Gateway**: Handles high traffic and routes booking requests.  
- **Lambda Functions**: Execute booking logic, verify seat availability, and manage SQS queues.  
- **DynamoDB**: Maintains ticket inventory using **optimistic locking** to prevent double booking.  
- **ElastiCache**: Caches real-time seat data for faster lookups.  
- **SQS**: Queues requests during DynamoDB spikes to prevent dropped transactions.  

**Solution 2 – Hybrid Cloud (Burst Model)**  
- **Route 53**: Routes between on-prem and AWS resources dynamically based on load.  
- **On-Prem Servers**: Handle standard demand for cost efficiency.  
- **AWS EC2 + Auto Scaling**: Activates during high-demand periods.  
- **DMS (Database Migration Service)**: Synchronizes data between on-prem and cloud databases.  
- **SQS + Lambda**: Process queued requests and maintain user responsiveness during transitions.  

---

## **💰 Cost Analysis**

| Cost Category | On-Prem | Hybrid | Full Cloud |
|----------------|----------|---------|-------------|
| Hardware & Refresh | $7.5M | $2.5M | $0 |
| IT Staffing | $350K | $200K | $100K |
| Power & Cooling | $1.96M | $981K | $0 |
| AWS Compute | $0 | $24K | $300K |
| AWS Storage | $0 | $75K | $150K |
| Total 5-Year Cost | **$20.98M** | **$9.93M** | **$4.98M** |

📊 *Full Cloud Migration reduces 5-year TCO by over 75% compared to on-prem.*  

---

## **📈 Compare & Contrast**

**Hybrid Cloud (On-Prem + AWS Cloud)**  
✅ Leverages existing infrastructure and ensures compliance.  
✅ Reduces downtime during migration.  
❌ Increases complexity and dual management overhead.  

**Full Cloud (AWS-Only)**  
✅ Offers scalability, automation, and built-in redundancy.  
✅ Minimizes hardware and maintenance costs.  
❌ Requires initial refactoring and dependency migration effort.  

---

## **🎯 Why**
This project demonstrates practical **cloud architecture design**, **cost modeling**, and **decision-based engineering**.  
It reflects the ability to balance **scalability, reliability, and financial efficiency** while leveraging **AWS-managed services** to modernize enterprise systems.  

---
