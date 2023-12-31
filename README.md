
# Should This Loan be Approved or Not? 💸



## Problem Importance 💡
#### Significance: 📈
In our loan approval project, our main goal is to predict the likelihood of a small or medium-sized business not being able to pay back the loan. This is crucial for our bank because if these businesses can't repay, banks might face financial losses. To achieve this, we're using a large set of data from past loan applications. We're looking for patterns or characteristics in these applications that can tell us if a loan is more or less likely to end in a situation where the business can't repay. This predictive model will help us make smarter decisions about which loans to approve, reducing the risk of financial problems for the banks. 
#### Consequences of Incorrect Decisions: ⚠️
Incorrect decisions in loan approvals can have profound consequences. Approving loans to high-risk applicants may lead to increased default rates, financial losses, and potential systemic impacts. On the other hand, unnecessary rejections can limit credit access for deserving individuals, hindering economic development. 
## Data 📊

Dataset: https://www.kaggle.com/datasets/mirbektoktogaraev/should-this-loan-be-approved-or-denied

The dataset used is obtained from Kaggle. It contains information on past loan applications made by small businesses, with various attributes like loan amount, location, industry sector, employment details, loan status etc.

Some key columns: 🗂

- Loan Number: Unique ID for loan application
- Customer Name: Name of loan applicant
- City, State, Zip: Location details
- Bank Name: Name of bank receiving the application
- NAICS Code: Industry code for applicant's business
- Term: Requested loan term
- MIS Status: Current status of the loan e.g. Paid In Full, Charged Off
- SBA Approved Amount: Loan amount approved by SBA
## Problem Analysis 🧐
#### Methodology: 📊
The analysis employed a two-fold approach, utilizing both Logistic Regression and Random Forest models. Logistic Regression provided a baseline, while the Random Forest model demonstrated superior predictive power.

#### Features and Preprocessing: ⚙️
- Selected Features: 📋
![Selected Features](https://github.com/jatinkam/Should-This-Loan-be-Approved-or-Not/assets/113269173/cf737c31-d894-4918-9545-d8f42e80abd8)

- Preprocessing Steps: 🧹
Handled missing values: Dropped rows or imputed values based on the nature of missing data.

Scaled numeric features: StandardScaler was applied to ensure uniform scales.

Derived features: 'DEFAULT' was created to represent loan outcomes.
![Preprocessing Steps](https://github.com/jatinkam/Should-This-Loan-be-Approved-or-Not/assets/113269173/4d0d9146-842c-4950-bcf0-efa5bbc3a2af)

## Findings and Visualization 📈
#### Exploratory Data Analysis 📊

![v1](https://github.com/jatinkam/Should-This-Loan-be-Approved-or-Not/assets/113269173/c8e9948c-05eb-446e-a456-5380719ebee5)

Based on the graph, it is evident that sectors 52 and 53 have a higher likelihood of loan default, while sectors 11 and 21 demonstrate a higher rate of customers successfully repaying their loan amounts in full.

![v2](https://github.com/jatinkam/Should-This-Loan-be-Approved-or-Not/assets/113269173/d8e07a07-d03f-4c41-837d-9c07fc371008)

This graph provides an overview of the number of loan applications within each specific sector.

#### Models 🤖
The Random Forest Classifier outperforms Logistic Regression in terms of accuracy and overall predictive performance, as evidenced by higher precision, recall, and F1-scores for both classes.

Logistic Regression has a higher precision for non-events, but Random Forest has a better overall balance between precision and recall for both classes.

Random Forest shows a significant improvement in identifying actual events compared to Logistic Regression.

Depending on the specific goals and considerations, the Random Forest Classifier may be a better choice for this classification task.

![model](https://github.com/jatinkam/Should-This-Loan-be-Approved-or-Not/assets/113269173/5e54f01f-285f-4bf3-91be-d472f2eb2ce8)

#### Correlation Matrix Heatmap 🗺️
#### Key Relationships: ➰
Positive correlations with 'REALESTATE,' 'DISBURSEMENTGROSS,' and 'PORTION.' ⬆️

Negative correlations with 'RETAINEDJOB' and 'URBANRURAL.' ⬇️

#### Insights: 💡
Loans associated with real estate, higher disbursement amounts, and specific portions of the approved amount have a higher likelihood of default.

![CMH](https://github.com/jatinkam/Should-This-Loan-be-Approved-or-Not/assets/113269173/1c8b03d1-bc7f-4e39-bf7f-9560ce3355c4)




## Conclusion  ✅

Exploratory Data Analysis and machine learning models, particularly the Random Forest, offer nuanced insights into loan repayment patterns. Implementing these insights in lending decisions enhances the ability to assess creditworthiness accurately. This data-driven approach contributes to responsible lending practices, minimizing risks and promoting economic stability. 📈