# A-B-Testing-Analysis

## Project Overview
This project analyzes an A/B test from the mobile game Cookie Cats, looking at what happens when the first time-gate is moved from level 30 to level 40. The notebook evaluates the results through two main lenses: long-term player retention and engagement-driven monetization.

## Trustworthy Experimentation
The analysis applies core concepts from Ron Kohavi's *Trustworthy Online Controlled Experiments*, including:
- A binomial test to check for Sample Ratio Mismatch (SRM)
- Defining an Overall Evaluation Criterion (OEC) that aligns with business objectives
- Using framing concepts like primary metrics and guardrails

## Data and Methodology
The dataset includes 90,189 players. To handle extreme outliers in player engagement, I used a log transformation alongside Interquartile Range (IQR) filtering. The statistical approach includes:
- **Two-Proportion Z-Test**: Used to check for significant differences in 1-day and 7-day player retention
- **Permutation Test**: Applied to handle the heavily skewed game rounds data without relying on strict normality assumptions
- **Bootstrapping**: Used to estimate a 95% confidence interval for the mean difference in engagement volume
