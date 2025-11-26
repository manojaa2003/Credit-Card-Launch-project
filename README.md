# Credit-Card-Launch-project
A complete end-to-end Data Cleaning, Statistical Analysis, and Financial Product Evaluation project.

#📘 Overview

This project simulates real-world Banking & Financial Services (BFSI) analytics using customer credit data from Atliqo Bank.
It is divided into two major phases:

Phase 1: Data Cleaning, Preprocessing & Outlier Handling

Phase 2: Statistical A/B Testing & Business Recommendations

This case study comes from Codebasics – Math & Statistics course.

#🔶 Phase 1 — Data Cleaning & Preprocessing
##🎯 Objective

Prepare raw banking data into a clean, validated, analysis-ready dataset.

##📝 Dataset Understanding

The dataset includes:

Customer demographics

Credit limit & outstanding debt

Employment type

Spending and transactions

Credit score & delinquency indicators

##🧹 Missing Value Treatment
##🔍 Missing Columns
->credit_limit

->age

->annual_income

->Certain categorical fields

##🧠 Imputation Logic

###Numeric features:
Group-wise mode imputation using (employment type × credit score range)

###Categorical features:
Mode imputation based on customer groupings

This ensures domain-consistent values.

📉 Outlier Detection
🛑 Domain-Based Outliers

Removed records where outstanding_debt > credit_limit

📊 Visualization-Based Outliers

Boxplots

Distribution plots

Numeric boundary checks

##📦 Final Output of Phase 1

Multiple cleaned dataset versions:

df_cs_clean_1

df_cs_clean_2

df_cs_clean_3 (final)

#🔶 Phase 2 — Statistical A/B Testing
##🎯 Objective

Evaluate whether a new credit card variant increases customer monthly spending.

⚙️ Feature Engineering

Constructed key analytical fields:

avg_spends

annual_transacts

control_group_avg_tran

test_group_avg_tran

These quantify customer spending behavior.

##📊 Descriptive Statistics

Compared control vs. test groups using:

Mean

Variance

Standard deviation

Distribution shape

##🧪 Hypothesis Testing — Two-Sample Z-Test
###📘 Hypothesis Formulation

H₀ (Null): Test group average spend ≤ Control group

H₁ (Alternative): Test group average spend > Control group (right-tailed)

##🧮 Results

Z-score > Critical Z-value

p-value < 0.05

##✔ Conclusion

Reject H₀ — the new credit card variant significantly increases average monthly spending.

##🔁 Validation

Performed a second test using statsmodels.stats.weightstats.ztest to confirm the results.

##🎯 Key Skills Demonstrated
##🟧 Data Engineering

Data Cleaning

Group-wise Mode Imputation

Outlier Detection

Feature Engineering

##🟦 Statistics & Modeling

A/B Testing

Z-Test

Hypothesis Testing

Descriptive Statistics

##🟩 Visualization

Boxplots

Histograms

Comparative Group Analysis

##🟪 Banking Domain Knowledge

Credit Risk Analytics

Spending Behavior Analysis

Product Evaluation & Recommendation

##🛠️ Tech Stack

Python

Pandas

NumPy

Matplotlib

Seaborn

Statsmodels

Jupyter Notebook

##📈 Business Outcome

The statistical analysis proves that the new credit card variant yields higher customer spending, making it a strong candidate for rollout.

