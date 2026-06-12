# youtube_trending_pipeline

Built an end-to-end AWS Data Pipeline that ingests YouTube trending data, transforms raw data into analytics-ready datasets using a Bronze-Silver-Gold architecture, and enables insights through Amazon Athena.

# Pipeline architecture
```text
┌─────────────┐   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐
│ YouTube API │ → │ Bronze (S3) │ → │ Silver (S3) │ → │ Gold (S3)   │
└─────────────┘   └─────────────┘   └─────────────┘   └──────┬──────┘
                                                              │
                                                              ▼
                                                     ┌─────────────┐
                                                     │ AWS Athena  │
                                                     └──────┬──────┘
                                                            │
                                                            ▼
                                                     ┌─────────────┐
                                                     │ Analytics & │
                                                     │ Insights    │
                                                     └─────────────┘
```
# AWS Architecture
<img width="2784" height="1536" alt="YouTube Trending Data Pipeline" src="https://github.com/user-attachments/assets/5099723e-323c-4d09-b24c-6e774d486d92" />

# 📊 Business Impact

Region-wise Trending Analysis
Channel Performance Tracking
Category Popularity Insights
Engagement Rate Monitoring
Historical Trend Analysis

# 🛠️ AWS Servies used

## 🛠️ AWS Services Used

| Service | Purpose |
|----------|---------|
| Amazon S3 | Stores raw, cleaned, and analytics-ready data. |
| AWS Lambda | Automates data ingestion and event-driven processing. |
| AWS Glue | Performs ETL transformations and cataloging. |
| AWS Athena | Enables serverless SQL analytics. |
| AWS Step Functions | Orchestrates the complete pipeline workflow. |
| Amazon SNS | Sends alerts and notifications. |
| Amazon CloudWatch | Monitors logs and pipeline health. |
| AWS IAM | Manages security and permissions. |

# 📂 Data Lake Layers
🥉 Bronze Layer
Stores raw YouTube data exactly as received.

🥈 Silver Layer
Cleaned and standardized datasets.

Transformations:
Null Handling
Schema Enforcement
Data Type Conversion
Deduplication
Derived Metrics

🥇 Gold Layer
Business-ready analytics tables.

Generated Tables:
trending_analytics
channel_analytics
category_analytics

# 👨‍💻 Author

Jay Nigam
Aspiring Data Engineer
GitHub: https://github.com/jaynigam7
LinkedIn: https://www.linkedin.com/in/jay-nigam
