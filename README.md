# Financial-Analytics-Project (Year 3 Sem 1) (2023)
# Credit Scorecard Solution for Fintech Lender

## Objective
This project aims to develop a credit scorecard model for a fintech lender, targeting underserved young adults (aged 20-35). The goal is to identify key factors that predict loan default and provide insights for responsible lending, while improving access to credit for millennials and young entrepreneurs.

## Business Opportunity
Traditional credit scoring methods often misjudge young adults due to limited credit history, irregular income streams, and lack of savings. Our solution focuses on leveraging alternative factors such as education level and potential income, to better assess creditworthiness. With the rising popularity of peer-to-peer lending and entrepreneurial goals, this presents a significant opportunity to expand the company's loan portfolio.

## Data Exploration & Preparation
We started with a dataset of 307,511 rows, narrowed down to 42,524 rows for our target segment (20-35-year-olds). Key steps included:

- **Data Cleaning:** Identified and removed invalid outliers and missing data, dropping columns with over 50% missing data.
- **Feature Selection & Extraction:** Selected relevant variables based on correlation analysis. Performed feature extraction to create new variables like `EXCESS_LOAN` and `SUM_PHONE_FLAGS` to enhance predictive power.

## Scorecard Construction
We constructed a logistic regression model with Weight of Evidence (WOE) binning for key variables. The final scorecard used the top 15 variables, including key financial and personal factors like total income and external credit scores. The model was trained and tested on 70%/30% split data and achieved an AUC of 0.7463.

## Model Evaluation
The top 15-variable model demonstrated a precision of 0.7 for default prediction and 0.67 for non-default. Various models were tested, and manual binning of certain variables like `AMT_ANNUITY` improved the scorecard's performance marginally.

## Challenges & Improvements
Key challenges included imbalanced data and precision tuning, but through feature engineering, we improved the precision from 67% to 70%. To enhance the model further, we recommend additional data acquisition, balancing techniques like SMOTE, and deeper client engagement to refine the model according to specific business needs.

## Future Work
- Incorporating more diverse datasets to improve model generalizability.
- Applying SMOTE to address data imbalance.
- Tailoring the scorecard with direct feedback from the client regarding their risk tolerance and precision targets.

## Conclusion
This credit scorecard solution presents an opportunity to expand loan access to young adults while maintaining responsible lending practices. Through careful data preparation, feature engineering, and model evaluation, we have developed a robust scorecard ready for further enhancement and real-world application.
