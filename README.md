# Credit Data Exploration with SQL

**Financial analytics • Customer segmentation • SQL • AWS Athena • Amazon S3**

An exploratory SQL case study of bank-customer profiles, credit limits, and transaction activity. The analysis turns business questions into queries and documents findings in a readable notebook.

## Problem

How do customer salary ranges, card types, and transaction behavior vary across a credit portfolio? Which data-quality issues should be understood before interpreting customer segments?

## Data

The notebook documents a sample of **2,564 records** from the EBAC course credit dataset, with customer demographics, salary ranges, card types, credit limits, and 12-month activity measures.

- Source: [EBAC course datasets](https://github.com/andre-marcos-perez/ebac-course-utils/tree/main/dataset).
- Salary values are ranges, not exact annual incomes.
- Some categorical fields use `na` to represent missing information.
- This is an educational analysis, not a production customer portfolio.

## Methodology

1. Inspect row counts, sample records, and column types.
2. Explore distinct categories and missing-value markers.
3. Aggregate customer counts by salary range and gender.
4. Compare minimum and maximum credit limits by education, card type, and gender.
5. Compare average product counts, transaction values, and credit limits by salary range.

## Technologies

**SQL, AWS Athena, Amazon S3, Jupyter / Google Colab.** The notebook presents SQL queries, screenshots, and interpretations; it is not an automated Python analysis pipeline.

## Findings and business interpretation

- The notebook reports that the largest salary segment is below 40K and that 235 records lack a salary range. This highlights both segment concentration and a data-completeness issue.
- Lower salary ranges are associated with lower average credit limits in the analyzed sample.
- Credit-limit comparisons show differences across the recorded groups. These descriptive patterns require deeper analysis before supporting a policy or customer decision.

The findings can inform follow-up questions about customer segmentation, data quality, and portfolio behavior. They do not establish causation or justify lending decisions based on demographic attributes.

## Explore the analysis

Open [Credit_EDA_and_Analysis.ipynb](Credit_EDA_and_Analysis.ipynb) for the SQL queries, recorded outputs, and discussion. Reproducing the queries requires access to the source data and an Athena table named `credito`; the repository does not include a complete infrastructure setup.
