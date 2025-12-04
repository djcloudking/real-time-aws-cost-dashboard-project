# Real-Time AWS Cost Dashboard

A hands-on project to **track, visualize, and optimize AWS costs** using Budgets, SNS, Lambda, and QuickSight. This dashboard provides real-time insights into your AWS spending and can alert you when your costs exceed predefined thresholds.

---


## Project Overview

This project demonstrates how to:
- Monitor AWS costs by service and tag
- Automate alerts when spending exceeds budget
- Visualize historical and real-time cost trends
- Implement cost-saving strategies with proactive notifications

The goal is to showcase **AWS cost optimization skills** and best practices in cloud governance.

---


## High Level Architecture (AWS Services I used)

- **AWS Budgets** – Track costs and set alerts  
- **Amazon SNS** – Notification service for alerts  
- **AWS Lambda** – Automate alerts and calculations  
- **CloudWatch Events** – Schedule Lambda executions  
- **Amazon QuickSight** – Interactive dashboards  
- **Amazon S3** – Store cost and usage reports  

---


## What I built (features)

- Real-time AWS cost monitoring
- Automated notifications via SNS (email/SMS)
- Interactive QuickSight dashboard for historical and daily costs
- Cost breakdown by service and environment
- Lambda automation for proactive alerts
- Supports tagging for cost allocation

---


## Setup & Installation

1. **Clone the repo**
```bash
git clone https://github.com/djcloudking/real-time-aws-cost-dashboard.git
cd real-time-aws-cost-dashboard
```

2. **Set up AWS Budgets**

- Create a monthly cost budget in the AWS Billing Console

- Set an alert threshold (e.g., 80%)


3. **Create SNS topic**

- Subscribe your email/SMS to receive alerts


4. **Configure Lambda**

- Upload lambda_alert.py (provided in this repo)

- Set environment variables:
  - AWS_ACCOUNT_ID
  - SNS_TOPIC_ARN
  - BUDGET_NAME

- Attach IAM permissions: ***Budgets:ViewBudget***, ***SNS:Publish***


5. **Schedule Lambda**

- Create a CloudWatch Event to trigger the Lambda daily


6. **Set up QuickSight Dashboard**

- Connect to your Cost & Usage Reports in S3

- Create visualizations for:
  - Daily costs by service
  - Top 5 expensive services
  - Costs by tag
  - Budget vs actual spend


## Usage

- Receive automated alerts when your AWS spend exceeds thresholds

- View the QuickSight dashboard for a visual breakdown of costs

- Adjust budgets, thresholds, or tags as needed


## Screenshots

Find every screenshots of my QuickSight dashboard, Lambda logs, and SNS alerts here: https://cloudwithdj.com/


