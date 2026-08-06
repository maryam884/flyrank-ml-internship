# Content Refresh Opportunity Scoring Using Search Performance Data

**Author:** Maryam Asif  
**Lane:** Refresh / Content Opportunity Scoring  
**Repository:** https://github.com/maryam884/flyrank-ml-internship  
**Date:** August 2026

0. Abstract

This research investigates how content pages can be prioritized for refresh opportunities using search performance data. The analysis uses the FlyRank ML Internship dataset containing anonymized production search signals. A content opportunity scoring approach was developed using performance features and compared against a baseline ranking method. The evaluation measures how the proposed approach compares with the baseline on the same validation split. The final output is a decision-support ranking system that helps content teams prioritize pages for refresh, expansion, protection, or monitoring.

1. Problem framing

This project supports the decision of which content pages should be prioritized for review and improvement.

The unit of analysis is a content page. The output is a priority score/ranking that identifies pages with higher content opportunity. A human editor can use this ranking to decide which pages should be refreshed, expanded, protected, or monitored.

A wrong decision may cause time and resources to be spent on pages with lower potential while missing valuable opportunities. Machine learning helps because the dataset contains millions of search performance records that cannot be manually analyzed one by one.

2. Data safety

The project uses the FlyRank ML Internship Dataset, a pseudonymized production search data release.

The analysis uses aggregated content and search performance information from the available tables, including content metadata and daily/query performance tables.

To keep the work public-safe, client names, URLs, raw search queries, and any identifying information were excluded. Pseudonymous identifiers were not used as model features and were only considered for grouping or validation purposes where needed.

Potential leakage risks were reviewed, especially fields derived from future outcomes such as trend_direction and trend_pct. These types of fields were excluded when they could reveal the target information directly.

No client-identifying details or private data are included in the report or repository outputs.

3. Baseline

The baseline is a simple ranking rule used as a transparent comparison before applying a more complex approach.

The baseline ranks pages using basic search performance signals available in the dataset. This provides a fair comparison because the model should demonstrate improvement over a simple rule using the same validation data and evaluation metrics.

The baseline results are measured on the same split used for the proposed approach.

4. Model / analysis

The project uses a content opportunity scoring approach to rank pages based on their potential need for improvement.

The method uses search performance features such as impressions, clicks, engagement signals, and historical performance indicators.

The target represents a content opportunity signal: identifying pages that may benefit from refresh or optimization.

Features that could directly reveal future outcomes were excluded to reduce leakage risk. The approach is designed for ranking and prioritization rather than making guaranteed predictions.

5. Evaluation

A validation split was designed to evaluate the approach on unseen data while reducing the risk of information leakage.

The model and baseline were compared using the same validation data and evaluation metrics.

The results measure ranking performance differences between the proposed approach and the baseline.

Error analysis showed that some pages are difficult to rank because of limited historical data, unstable performance patterns, or unusual engagement behavior.

The output should be interpreted as decision-support rather than an automatic decision system.

6. Interpretation

The analysis shows that search visibility and engagement-related signals provide useful information for identifying content opportunities.

Pages with strong visibility but weaker engagement signals may represent opportunities for improvement.

The model captures patterns in the available performance data, but some pages remain difficult to rank because their behavior does not follow common patterns.

These findings are directional observations and should be used to support human decision-making.
7. Recommendation

The ranked output supports the following action playbook:

1. Refresh pages with high visibility but lower engagement signals.
2. Expand pages showing potential based on search interest and performance patterns.
3. Protect consistently strong-performing pages.
4. Monitor pages where available evidence is limited.

These recommendations are intended to help content teams prioritize work. They are decision-support suggestions and do not guarantee future performance improvements.

8. Reproducibility

The analysis can be reproduced using the notebooks available in the repository.

Notebook:
work/notebooks/capstone.ipynb

Supporting notebooks:
- Research question definition
- Data contract and safety checks
- Baseline analysis
- Feature analysis
- Model development
- Validation audit
- Action playbook

The experiments were run using the documented notebook environment and workflow.

## Acknowledgments & Data Credit

Built on the FlyRank ML Internship Dataset.

Data source: https://flyrank.ai

This project uses the anonymized FlyRank ML Internship dataset for educational purposes. No client-identifying information is included.
