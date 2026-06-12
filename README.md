# youtube_trending_pipeline

Built an end-to-end AWS Data Pipeline that ingests YouTube trending data, transforms raw data into analytics-ready datasets using a Bronze-Silver-Gold architecture, and enables insights through Amazon Athena.

# Pipeline architecture

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

# AWS Architecture
<img width="2784" height="1536" alt="YouTube Trending Data Pipeline" src="https://github.com/user-attachments/assets/5099723e-323c-4d09-b24c-6e774d486d92" />

# 📊 Business Impact

Region-wise Trending Analysis
Channel Performance Tracking
Category Popularity Insights
Engagement Rate Monitoring
Historical Trend Analysis

# 🛠️ AWS Servies used

| Service | Logo | Purpose |
|----------|------|---------|
| Amazon S3 | <img src="https://raw.githubusercontent.com/simple-icons/simple-icons/develop/icons/amazons3.svg" width="30"> | Stores raw, cleaned, and analytics-ready data across Bronze, Silver, and Gold layers. |
| AWS Lambda | <img src="https://raw.githubusercontent.com/simple-icons/simple-icons/develop/icons/awslambda.svg" width="30"> | Automates data ingestion and event-driven processing tasks. |
| AWS Glue | <img src="https://cdn.worldvectorlogo.com/logos/aws-glue.svg" width="30"> | Performs ETL transformations and metadata cataloging. |
| AWS Athena | <img src="https://cdn.worldvectorlogo.com/logos/aws-athena.svg" width="30"> | Enables serverless SQL analytics on processed datasets. |
| AWS Step Functions | <img src="https://cdn.worldvectorlogo.com/logos/aws-step-functions.svg" width="30"> | Orchestrates the complete data pipeline workflow. |
| Amazon SNS | <img src="https://cdn.worldvectorlogo.com/logos/aws-sns.svg" width="30"> | Sends alerts and notifications for pipeline events. |
| Amazon CloudWatch | <img src="https://cdn.worldvectorlogo.com/logos/aws-cloudwatch.svg" width="30"> | Monitors logs, metrics, and pipeline health. |
| AWS IAM | <img src="https://cdn.worldvectorlogo.com/logos/aws-iam.svg" width="30"> | Manages security and access permissions. |

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
