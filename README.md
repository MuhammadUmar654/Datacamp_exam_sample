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

## Key Findings

### 1. Leisure travellers generate more ancillary revenue

| Metric | Business Guests | Leisure Guests |
|---|---:|---:|
| Total ancillary revenue | $23,614.53 | $31,937.89 |
| Purchasing guests | 123 | 151 |
| Average spending per purchasing guest | $191.99 | $211.51 |

Leisure travellers contribute more total revenue and demonstrate slightly higher average spending than business travellers.

Approximately 8.36% of revenue could not be classified by travel purpose because matching stay information was unavailable.

### 2. Revenue contribution and spending intensity tell different stories

Guests without a loyalty tier collectively generate the most ancillary revenue, largely due to their higher representation among purchasers.

However, Platinum guests have the highest average ancillary spending.

At the combined segment level:

- **Highest total revenue:** Leisure travellers without a loyalty tier, approximately $10,900.
- **Highest average spending:** Platinum leisure travellers, approximately $400 per purchasing guest.

This distinction highlights why both segment size and average customer spending matter when prioritising business opportunities.

### 3. Loyalty tier has a statistically significant positive association with spending

A one-sided Spearman rank correlation test produced:

| Statistic | Result |
|---|---:|
| Spearman's rho | 0.2265 |
| P-value | 0.00000965 |
| Significance level | 0.05 |

The result indicates a **weak but statistically significant positive association** between loyalty tier and total recorded ancillary spending among purchasing guests.

This relationship is observational and does not establish that increasing a guest's loyalty tier will cause them to spend more.

### 4. Guests without recorded purchases represent a potential opportunity

Among 400 guest profiles:

- 349 guests had recorded ancillary purchases.
- 51 guests had no recorded ancillary purchases.
- 42 of those 51 guests had marketing consent.

The hotel-wide recorded ancillary purchase participation rate was **87.25%**.

Guests without recorded purchases were treated as non-purchasers for this analysis, although incomplete transaction records cannot be ruled out.

### 5. Hypothetical revenue-growth scenarios

To estimate the potential opportunity among the 42 eligible guests, three conversion scenarios were modelled using average spending benchmarks from existing purchasers within the same loyalty tiers.

| Assumed Conversion | Potential Additional Gross Revenue | Uplift vs. Current Revenue |
|---|---:|---:|
| 10% | $676.41 | 1.12% |
| 20% | $1,352.82 | 2.23% |
| 30% | $2,029.22 | 3.35% |

These are illustrative scenario estimates, not forecasts or observed campaign results. They assume similar spending behaviour among converted guests and exclude campaign costs.

## Business Recommendations

**Test targeted ancillary-service offers.** Run a small promotional pilot among eligible guests with no recorded purchases, prioritising appropriate marketing consent and measuring subsequent purchasing behaviour.

**Investigate loyalty enrolment opportunities.** Since higher loyalty tiers are associated with greater recorded spending, test whether loyalty-related incentives influence ancillary purchases. The existing correlation alone does not demonstrate a causal effect.

**Monitor conversion alongside revenue.** Track ancillary purchase participation and revenue per eligible guest rather than relying only on total revenue. Ideally, use a control group to estimate the campaign's incremental effect before expanding the initiative.

## KPIs

| KPI | Baseline or Measurement Approach |
|---|---|
| Total Ancillary Revenue | $60,619.89 |
| Ancillary Purchase Participation | 87.25% of profiled guests |
| Campaign Conversion Rate | Measure during a future campaign |
| Incremental Ancillary Revenue | Estimate against a suitable control group |

## Tools and Technologies

- **SQL / Google BigQuery:** Data cleaning, preparation, and validation
- **Python / Pandas / NumPy:** Data manipulation and guest-level aggregation
- **Matplotlib / Seaborn:** Exploratory visualisations and segment comparisons
- **SciPy:** Spearman rank correlation hypothesis testing
- **Google Colab:** Analysis notebook and documentation

## Project Files

- [Python Analysis Notebook](./Datacamp_exam.ipynb) — Data exploration, guest segmentation, statistical analysis, and revenue modelling.
- **Written Analysis Report** — Detailed visual findings, methodological explanations, KPI definitions, and business recommendations (PDF included in this repository).

## Limitations

This analysis has several important limitations:

- Ancillary transactions are associated with guests rather than individual stays, preventing reliable stay-level attribution.
- Some guest spending could not be classified by travel purpose.
- Guests without recorded purchases were assumed to be non-purchasers for opportunity modelling.
- Statistical association does not imply causation.
- Revenue-growth scenarios rely on assumptions rather than observed campaign performance.

## Conclusion

The analysis demonstrates that ancillary revenue performance depends on both guest-segment size and individual spending intensity.

Leisure travellers and non-tier guests contribute substantial total revenue, while premium loyalty segments demonstrate higher average spending.

The most immediate opportunity identified is to investigate ancillary purchase conversion among eligible guests with no recorded spending, supported by targeted experiments and measurable business KPIs.

The project illustrates how exploratory analysis, statistical reasoning, and scenario modelling can turn transactional data into actionable business recommendations.

---

**Project type:** DataCamp Data Analyst Certification — Sample Practical Exam

**Author:** Muhammad Umer Mustafa

**Focus:** Data Analytics · Customer Segmentation · Revenue Optimisation · Marketing Analytics
