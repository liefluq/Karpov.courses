# Product & Data Analytics Portfolio

**Overview**
This repository contains applied data analytics projects focused on A/B testing, SQL-based CRM segmentation, and Python ETL automation for product metrics. 

## Project Product analytics: A/B Testing Analysis for Payment Mechanics
* **Goal:** Evaluate the impact of a new payment mechanic on conversion rates (CR) and average revenue (ARPU/ARPPU) to determine the feasibility of a global rollout.
* **Tech Stack:** Python (pandas, SciPy, Seaborn, Matplotlib).
* **Key Results:**
  * Performed rigorous data cleaning, identifying and filtering out anomalous tracking logs (e.g., payments without active sessions).
  * Conducted statistical hypothesis testing using Chi-Square for categorical CR and Welch's t-test / Mann-Whitney U test for continuous ARPPU distributions.
  * Applied Bootstrap to calculate 95% Confidence Intervals for ARPU due to zero-inflated, highly asymmetrical data distributions.
  * Detected a critical Sample Ratio Mismatch (SRM), leading to a data-driven recommendation to halt the rollout and audit the traffic split mechanism before further testing.

## Project FINAL: E-commerce CRM Segmentation & Metric Automation
* **Goal:** Build a robust data mart for CRM communications and automate the recalculation and visualization of key product metrics using incremental data.
* **Tech Stack:** SQL (CTEs, Window Functions), Python (pandas, Matplotlib, Seaborn).
* **Key Results:**
  * Developed a modular SQL architecture using CTEs to segment customers into 'Loyal', 'One-time', 'New', and 'Inactive' cohorts based on transaction history and registration recency.
  * Implemented Data Quality checks to ensure chronological consistency of order and delivery logs prior to segmentation.
  * Created an automated Python pipeline to dynamically merge baseline and incremental datasets, handle schema variations, recalculate CR, ARPU, and ARPPU, and generate presentation-ready comparative visualizations for business stakeholders.
