# Datacamp_exam_sample
# Hotel Ancillary Revenue Analysis
### Guest Segmentation | Revenue Analytics | Statistical Testing | Business Intelligence

**Python · SQL · Google BigQuery · Pandas · Seaborn · SciPy**

## Project Overview

How can a hotel identify its most valuable guest segments and uncover opportunities to increase revenue beyond room bookings?

This project analyses ancillary revenue at **Solstice Opal Hotel**, focusing on guest spending across dining, spa, and activities.

The objective was to understand which guest segments contribute the most revenue, investigate differences in spending behaviour, and identify potential revenue-growth opportunities through data-driven recommendations.

The project covers the end-to-end analytical process, from data preparation and exploratory analysis to hypothesis testing, KPI development, and business recommendations.

## Business Problem

Hotel management observed significant differences in ancillary spending across guests but lacked a clear understanding of:

- Which guest segments generate the most ancillary revenue?
- How do spending patterns differ across loyalty tiers and travel purposes?
- Is there a statistically significant relationship between loyalty tier and spending?
- Where could the hotel capture additional revenue?
- Which KPIs should management monitor to evaluate improvement?

## Dataset

The analysis uses three interconnected datasets:

| Dataset | Description |
|---|---|
| Guest Profiles | Guest identifiers, loyalty tiers, and marketing consent |
| Stay Details | Travel purpose, booking channel, guest count, and stay information |
| Ancillary Spend | Guest-level transactions covering dining, spa, and activities |

The source data was cleaned using SQL in Google BigQuery, followed by exploratory analysis and statistical testing in Python.

**Important limitation:** Ancillary transactions cannot be reliably attributed to individual stays. Revenue was therefore aggregated at the guest level before segmentation to avoid double-counting.

## Analytical Approach

**1. Data Preparation and Validation**

Data was cleaned and prepared using BigQuery, with attention to missing values, inconsistent identifiers, and join relationships. Guest-level aggregation was used to protect revenue calculations from duplicate records introduced by joins.

**2. Exploratory Data Analysis**

Examined spending distributions, outliers, total revenue, average spending per purchasing guest, and differences across travel-purpose and loyalty segments.

**3. Guest Segmentation**

Combined loyalty tier and travel purpose to distinguish segments generating the highest total revenue from those demonstrating the highest average spending.

**4. Statistical Hypothesis Testing**

Used Spearman's rank correlation to evaluate the association between loyalty tier and total recorded ancillary spending per purchasing guest.

**5. Revenue Opportunity Modelling**

Identified guests without recorded ancillary purchases, considered marketing consent, and developed hypothetical conversion scenarios based on existing purchaser spending benchmarks.

**6. KPI Development**

Defined the hotel's ancillary purchase participation baseline and proposed metrics to evaluate future revenue-growth initiatives.

## Tools and Technologies

- **SQL / Google BigQuery:** Data cleaning, preparation, and validation
- **Python / Pandas / NumPy:** Data manipulation and guest-level aggregation
- **Matplotlib / Seaborn:** Exploratory visualisations and segment comparisons
- **SciPy:** Spearman rank correlation hypothesis testing
- **Google Colab:** Analysis notebook and documentation

## Project Files

- [Python Analysis Notebook](./Datacamp_exam.ipynb) — Data exploration, guest segmentation, statistical analysis, and revenue modelling.
- **Written Analysis Report** — (https://github.com/MuhammadUmar654/Datacamp_exam_sample/blob/main/Final%20report)
- **Datasets and Emails from Managers**: https://github.com/MuhammadUmar654/Datacamp_exam_sample/blob/main/dataset_and_questions.pdf

## Limitations

This analysis has several important limitations:

- Ancillary transactions are associated with guests rather than individual stays, preventing reliable stay-level attribution.
- Some guest spending could not be classified by travel purpose.
- Guests without recorded purchases were assumed to be non-purchasers for opportunity modelling.
- Statistical association does not imply causation.
- Revenue-growth scenarios rely on assumptions rather than observed campaign performance.

---

**Project type:** DataCamp Data Analyst Certification — Sample Practical Exam

**Author:** Muhammad Umer Mustafa

**Focus:** Data Analytics · Customer Segmentation · Revenue Optimisation · Marketing Analytics
