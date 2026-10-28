# Product & Data Analytics Portfolio

## Overview

This repository contains educational projects completed as part of
the Data Analyst course at karpov.courses.

The projects cover A/B test analysis, SQL-based customer segmentation,
Python-based metric recalculation, cohort analysis, and product
hypothesis prioritization.

## 1. Final Project: A/B Test Analysis, CRM Segmentation
## and Metric Recalculation

Notebook: FINAL_project.ipynb

### Goal

Analyze an experiment involving a new payment flow, prepare a
customer segmentation dataset for CRM communications, and develop
reusable functions for recalculating and visualizing experiment metrics.

### Tech Stack

Python: pandas, NumPy, SciPy, Matplotlib, Seaborn.
SQL: CTEs, joins, aggregations, CASE expressions, date calculations.

### Main Tasks and Findings

#### A/B Test Analysis

- Combined experiment assignments, user activity, and payment data.
- Identified payments from users absent from the activity dataset,
  documented possible explanations, and restricted the main analysis
  to recorded active users.
- Calculated conversion rate, ARPU, and ARPPU for the control
  and treatment groups.
- Compared conversion rates using a chi-square test and mean revenue
  among paying users using Welch’s t-test.
- Used the Mann–Whitney U test as an additional rank-based comparison
  of payment distributions.
- Estimated a 95% bootstrap confidence interval for the difference
  in ARPU between the treatment and control groups.
- Found no statistically significant differences in CR or ARPU,
  while observing a statistically significant difference in ARPPU.
- Highlighted the need to verify the intended traffic allocation
  before drawing conclusions about sample ratio mismatch.

#### SQL Customer Segmentation

- Built a customer-level dataset using CTEs, aggregations,
  and LEFT JOINs.
- Assigned customers to Regular, Occasional, New, and Inactive
  segments based on delivered order counts and time since registration.
- Included purchase event counts and average delivery times
  in the segmentation dataset.
- Checked for orders with delivery timestamps earlier than
  their creation timestamps.
- Visualized the customer segment distribution and proposed
  CRM communication ideas.

#### Python Metric Recalculation

- Developed reusable functions to load and combine baseline
  and additional experiment assignment files.
- Supported selected CSV delimiter and column-name variations.
- Recalculated CR, ARPU, and ARPPU for recorded active users.
- Generated labeled charts comparing experiment groups.

## 2. Marketplace Product Analytics:
## Retention, Metrics and Hypothesis Prioritization

Notebook: Product_analytics.ipynb

### Goal

Explore customer retention and purchasing behavior in an e-commerce
marketplace, identify product improvement opportunities, and prioritize
hypotheses for further testing.

### Tech Stack

Python: pandas, NumPy, Matplotlib, Seaborn.

### Main Tasks and Findings

- Built monthly customer cohorts based on the month of first order.
- Calculated retention by cohort and visualized repeat ordering
  with a heatmap.
- Observed low monthly repeat-order retention in the analyzed data.
- Analyzed monthly GMV, purchasing customer counts, repeat purchasing,
  and GMV per purchasing customer.
- Explored geographic and delivery-related patterns.
- Prioritized three product hypotheses using the ICE framework.
- Proposed target, proxy, and guardrail metrics for a future
  experiment addressing order processing issues.

## Scope and Limitations

These are educational analyses, not production deployments.

Recommendations represent analytical proposals rather than
implemented business changes or measured business impact.

Experiment conclusions depend on the validity of the assignment
and activity data. Marketplace findings are limited to the available
order history and observation period.
