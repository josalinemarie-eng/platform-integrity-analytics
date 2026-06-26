# Platform Integrity Analytics

This repository houses data science initiatives focused on **platform integrity, trust & safety, and algorithmic accountability**. My work bridges the gap between abstract policy and production-ready code, demonstrating how machine learning can be used to mitigate operational risk, optimize moderation workflows, and safeguard user experiences on large-scale social platforms.

---

## Current Projects

### 1. [TikTok Profile Verification Prediction](notebooks/01_tiktok_verification_classifier.ipynb)
**Objective:** Build a baseline logistic regression framework to predict account verification status based on user behavior and video engagement metrics to optimize automated moderation routing.

* **Technical Approach:** I formulated a robust preprocessing pipeline to handle systemic logging gaps and feature-engineered text-metadata. To address the severe structural class imbalance—~93.7% unverified vs. ~6.3% verified—I implemented minority upsampling to ensure the model could effectively identify both classes.
* **Operational Insights:** The model achieved an **84% recall** in identifying unverified accounts. By analyzing model coefficients, I identified that video duration, comment volume, and the presence of opinion-based claims are strong indicators of unverified status, whereas high download volumes strongly correlate with established, trusted profiles.
* **Business Impact:** I proposed a risk-mitigation strategy centered on a **hybrid trusted-creator whitelist** (designed to eliminate a 61% precision bottleneck and protect the user experience) combined with an **automated triage review queue** to streamline high-volume backlogs.
* **Reproducibility Note:** All models were initialized with `random_state=0` to ensure consistency and reproducibility across experimental iterations.

---

## Repository Structure

```text
platform-integrity-analytics/
├── README.md             # Project index and operational documentation
├── notebooks/            # End-to-end pipelines and case studies
└── data/                 # Sample data schemas and processing manifestspplicable)
