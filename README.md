# platform-integrity-analytics
This repository contains case studies in platform integrity, risk mitigation, and algorithmic accountability.
# Platform Integrity Analytics

This repository houses a collection of data science projects focused on **platform integrity, trust & safety, and algorithmic accountability**. It demonstrates the application of machine learning to mitigate operational risk, optimize moderation workflows, and ensure a safer user experience on large-scale digital platforms.

---

## Current Projects

### 1. [TikTok Verification Status Classifier](notebooks/01_tiktok_verification_classifier.ipynb)
**Objective:** Build a logistic regression model to predict user verification status based on engagement and behavioral metrics.
* **Key Technicals:** Handled severe class imbalance (93.7% vs 6.3%) via downsampling; optimized feature selection to isolate high-impact behavioral drivers.
* **Operational Insight:** Identified that opinion-based content is a primary signal of verification, whereas high-velocity "claim" media often originates from unverified, higher-risk profiles.
* **Impact:** Proposed a risk-tiered moderation queue to prioritize human review for unverified, high-engagement content while whitelisting verified creators to reduce operational friction.

---

## Repository Structure
```text
platform-integrity-analytics/
├── README.md             # Project index and documentation
├── notebooks/            # Jupyter notebooks for each case study
├── requirements.txt      # Dependencies for reproduction
└── data/                 # Sample data/schemas (where applicable)
