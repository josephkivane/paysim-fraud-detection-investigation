# PaySim Financial Fraud Detection and Investigation

## Project Overview

This project investigates suspicious financial transactions using the PaySim synthetic mobile money transaction dataset. It combines SQL, Python, data analysis, feature engineering, and machine learning to examine transaction patterns associated with fraud-labelled and legitimate transactions.

The project uses a Random Forest classifier to identify suspicious transactions and evaluates its performance using precision, recall, F1-score, and chronological validation. It also examines false positives and false negatives to demonstrate how machine learning can support human-led financial fraud investigations.

## Project Objectives

- Investigate transaction patterns associated with fraud-labelled transactions.
- Use SQL and Python to explore transaction behaviour.
- Engineer features from transaction and account balance information.
- Develop a Random Forest fraud classification model.
- Evaluate model performance using appropriate classification metrics.
- Examine model alerts and discuss their implications for financial investigations.

## Tools and Technologies

- Python
- SQL (DuckDB)
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

## Key Findings

- Fraud-labelled transactions were concentrated in the TRANSFER and CASH_OUT transaction types.
- Transaction amount alone was not sufficient to distinguish fraudulent activity.
- Account balance behaviour provided useful information for identifying suspicious transactions.
- Chronological validation was used to assess performance on later transactions not used during training.

## Model Performance

The Random Forest model achieved the following results on the chronological test set:

| Metric | Result |
|---|---:|
| Precision | 99.91% |
| Recall | 99.74% |
| F1-score | 99.82% |
| False Positives | 4 |
| False Negatives | 11 |

## Important Limitations

- PaySim is a synthetic dataset, not real banking transaction data.
- The fraud labels are dataset-provided labels and do not represent independently verified criminal cases.
- Some engineered features use post-transaction information, making the current model more suitable for retrospective investigation than real-time fraud detection.
- Model alerts should support further investigation rather than be treated as proof of fraud.

## Project Files

- **Jupyter Notebook:** Contains the investigation, SQL/Python analysis, feature engineering, model development, and evaluation.
- **HTML Report:** An exported version of the notebook for convenient viewing.

## Dataset

PaySim Synthetic Financial Dataset: https://www.kaggle.com/datasets/ealaxi/paysim1

## Conclusion

This project demonstrates how data analysis, feature engineering, and machine learning can support financial fraud investigation. It highlights the importance of examining transaction behaviour, evaluating model errors, and using analytical results to guide further investigation.
