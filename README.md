# Platform Integrity Analytics

This repository houses data science initiatives focused on **platform integrity, trust & safety, and algorithmic accountability**. These projects demonstrate how machine learning can be used to mitigate operational risk, optimize moderation workflows, and safeguard user experiences on large-scale social platforms.

---

## Current Projects

### 1. [TikTok Profile Verification Prediction](notebooks/01_tiktok_verification_classifier.ipynb)
**Objective:** Build a baseline logistic regression framework to predict account verification status based on user behavior and video engagement metrics to optimize automated moderation routing.

* **Key Technicals:** Formulated a robust preprocessing pipeline including handling systemic logging gaps, feature engineering text-metadata lengths, and resolving a severe structural class imbalance (~93.7% unverified vs. ~6.3% verified) via minority upsampling.
* **Operational Insight:** Evaluated the model's performance trade-offs, achieving an **84% recall** for filtering unverified accounts. Discovered through model coefficients that video duration, comment volume, and opinion-based claims serve as strong indicators of unverified status, while high download volumes strongly correlate with trusted, verified profiles.
* **Business Impact:** Proposed an operational risk-mitigation strategy combining a **hybrid trusted-creator whitelist** (to eliminate a 61% precision bottleneck and protect creator experience) with an **automated triage review queue** to streamline high-volume backlogs.

---

## Repository Structure

```text
platform-integrity-analytics/
├── README.md             # Project index and operational documentation
├── notebooks/            # Jupyter notebooks containing end-to-end pipelinesach case study
├── requirements.txt      # Dependencies for reproduction
└── data/                 # Sample data/schemas (where applicable)
