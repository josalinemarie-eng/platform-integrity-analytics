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

## Phase 2: Exploratory Data Analysis & Predictive Modeling for Content Moderation

This phase expands beyond initial exploratory data analysis to build predictive machine learning workflows aimed at automated content moderation and account risk classification.

* **Core Objective:** Build a predictive classification workflow to identify unverified vs. verified account behaviors and high-risk claim profiles, optimizing content routing for human moderation review[cite: 3].
* **Data Cleansing & Integrity:** Handled missingness by removing non-random logging gaps across video engagement metrics, preserving 19,084 high-signal rows (~98.5% of total dataset)[cite: 3].
* **Class Imbalance Handling:** Addressed heavy target imbalance (~6.3% minority class) by executing oversampling techniques to achieve a balanced 50/50 target distribution prior to model training[cite: 3].
* **Feature Engineering:** Extracted character-level length metrics (`text_length`) from video transcription text to analyze structural variations in user claims across status cohorts[cite: 3].

* ---

## Next Steps : Transitioning to Project SOMA — From Exploration to Modular Architecture

Building directly upon the predictive patterns and data preprocessing frameworks established in Phase 2, this next phase transitions raw exploratory notebooks into **Project SOMA**—an open-source, modular AI content moderation and risk classification concept.

* **Framework Integration:** Translates static data cleansing and logistic regression classifiers into reusable Python modules (`src/`) designed for dynamic policy configuration and automated execution.
* **Dual-Pathway Routing Logic:** Implements an automated triage architecture that routes high-confidence risk predictions directly to mitigation workflows while queuing ambiguous edge cases for specialist review.
* **Scalable Trust & Safety Operations:** Bridges the gap between exploratory data science and production-minded risk governance, aligning machine learning outputs with enterprise content integrity guardrails.

---

## Repository Structure

```text
platform-integrity-analytics/
├── README.md             # Project index and operational documentation
├── notebooks/            # End-to-end pipelines and case studies
└── data/                 # Sample data schemas and processing manifests
