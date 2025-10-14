# Banking Risk Analytics — MySQL Database + Python EDA + Power BI Dashboard

## 1. Project Overview
End-to-end banking analytics project designed to understand **risk patterns** in lending and deposits.  
Objective: analyze customer data to identify segments with higher credit exposure and potential risk concentration.

**Problem Statement:**  
> Develop a basic understanding of risk analytics in banking and financial services, and explore how data is used to minimize the risk of losing money while lending to customers.

---

## 2. Tech Stack
| Component | Tool |
|------------|------|
| Database | MySQL |
| Data Analysis | Python (Google Colab) |
| Visualization | Power BI |
| Libraries | pandas, matplotlib, seaborn, pymysql |

---

## 3. Workflow
1. **Database Setup:** Created a MySQL database named `banking` and imported dataset (3000 rows × 25 columns).  
2. **Python Integration:** Connected MySQL with Python using `pymysql`.  
3. **Exploratory Data Analysis:** Cleaned, transformed, and visualized the dataset in Google Colab.  
4. **Dashboard Development:** Imported processed data into Power BI for final business-level insights.

---

## 4. Exploratory Data Analysis (Python - Google Colab)

### Notebook Access
Full Python notebook available here:  
🔗 [Open Colab Notebook](https://colab.research.google.com/drive/1y_h4gwhyG4emZpd1Ad2CtNyztcXmuGu6)

---

### Dataset Summary
- **Shape:** (3000, 25)  
- **Data Types:** 8 object, 8 integer, 9 float  
- **Memory Usage:** ~586 KB  
- Includes customer demographics, income, assets, loan amounts, and deposits.

---

### 4.1 Descriptive Statistics
Generated summary metrics for all numeric features to understand central tendency and spread.

**Insight:** 
Income and loan distributions were right-skewed — indicating a small subset of high-value clients.


### 4.2 Income Band Categorization

Created categorical segmentation of income into Low, Medium, and High tiers.

<img width="732" height="86" alt="image" src="https://github.com/user-attachments/assets/96303617-80a7-4857-ac6f-2d401d4ad0fb" />

**Insight**
High-income customers dominate, reinforcing Private Banking concentration.


### 4.3 Examine the distinction of unique categories in categorical columns

<img width="793" height="151" alt="image" src="https://github.com/user-attachments/assets/29dcbc2b-a81a-4048-a98c-f223f122e4c0" />

**Insight** 
- Count plots generated for each categorical variable.

- Assessed demographic distribution, customer segmentation, and loyalty tiers.

### 4.4 Bivariate and Univariate Analysis

**Univariate**: Frequency of each categorical variable.

**Bivariate**: Count plots showing relationships between predictors and GenderId for pattern detection.

**Objective**: Detect any gender or demographic bias in lending or deposits.


### 4.5 Categorical & Demographic Distribution

Plotted categorical variables like Gender, Occupation, Nationality, Fee Structure, and Risk Weighting.

<img width="365" height="201" alt="image" src="https://github.com/user-attachments/assets/bff705bf-c168-43ae-ae48-3b05a5f4d94c" />

**Insight** 
Most clients are professionals in technical or structural roles, consistent with high-income segmentation.


### 4.6 Numerical Feature Distribution

<img width="1146" height="208" alt="image" src="https://github.com/user-attachments/assets/60d91d20-ffee-497e-b1cb-bec64955ce44" />

- Visualized histograms with sns.histplot(kde=True)

- Identified skewness in loan and income distributions.


### 4.7 Correlation Heatmap

<img width="1092" height="187" alt="image" src="https://github.com/user-attachments/assets/52709d31-32ae-4c16-bd4d-049446c42c9f" />

**Insight**

- Strong positive correlation between Bank Deposits, Checking Accounts, and Saving Accounts.

- Business Lending and Bank Loans moderately correlated, indicating potential overlap in loan exposure.

- Credit Card Balance weakly correlated with total lending — suggests separate risk profile.

# POWER BI DASHBOARD ANALYSIS

## Calculated Functions

**Total Deposit**
Total Deposit = SUM(Banking[Bank Deposits]) + SUM(Banking[Saving Accounts]) + SUM(Banking[Foreign Currency Account]) + SUM(Banking[Checking Accounts])

**Total Loan**
Total Loan = SUM(Banking[Bank Loans]) + SUM(Banking[Business Lending]) + SUM(Banking[Credit Card Balance])

**Total Fees**
Total Fees = SUMX(Banking, Banking[Total Loan] * Banking[Processing Fees])

---
## Home Page

<img width="1105" height="592" alt="image" src="https://github.com/user-attachments/assets/420f96a4-eda7-46ac-9abc-b3b063a5c61a" />

## 1. Deposit Analysis

### Overview
Total deposits reached **$3.8 billion**, consisting of:
- **$2 billion** in bank deposits  
- **$963.3 million** in checking accounts  
- **$698.7 million** in savings accounts  

Deposits are primarily driven by **Private Banking** clients and **High-Income** segments.

### Key Findings
- **Banking Relationship:** Private Banks dominate, followed by Retail, Commercial, and Institutional clients.  
- **Income Band:**  
  - High Income: **~54% ($2.03B)**  
  - Medium Income: **~24% ($0.94B)**  
  - Low Income: **~21% ($0.80B)**  
- **Nationality:** European clients hold the majority, followed by Asian and American customers.  
- **Occupation:** Top contributors include Structural, Database, and Office Associates.  

### Interpretation
Deposit growth is concentrated among high-income and European clients, ensuring stability but indicating limited diversification. Retail and regional expansion could improve long-term balance and deposit resilience.

<img width="1112" height="623" alt="image" src="https://github.com/user-attachments/assets/eb239b11-ff03-4849-8518-2a6741a0a8d5" />

---

## 2. Loan Analysis

### Overview
Total loans amount to **$4.4 billion**, including:
- **$1.8 billion** in direct bank loans  
- **$2.6 billion** in business lending  
- **$9.5 million** in credit card balances  

Private Banks again lead in total lending, mirroring deposit concentration.

### Key Findings
- **Banking Relationship:** Private Banks dominate, followed by Retail, Commercial, and Institutional clients.  
- **Composition:** Business lending accounts for **~59%** of total loans, showing enterprise-heavy exposure.  
- **Income Band:**  
  - High Income: **53% ($942.49M)**  
  - Medium Income: **25% ($448.19M)**  
  - Low Income: **22% ($383.47M)**  
- **Nationality:** Majority from European borrowers; minor shares from Asian, American, Australian, and African clients.  
- **Occupation:** Major borrowers are Account Coordinators, Database Professionals, and Office Assistants.  

### Interpretation
Lending portfolio is strong and concentrated in high-value segments, ensuring quality but reducing diversification. Expanding into medium- and low-income demographics can increase volume and market spread without heavily increasing credit risk.

<img width="1120" height="628" alt="image" src="https://github.com/user-attachments/assets/1d430448-6604-4000-81fb-dc7dd737871d" />

---
## Summary Dashboard

<img width="1118" height="628" alt="image" src="https://github.com/user-attachments/assets/141ede67-8f8b-425e-91bb-2d53ecbbc115" />

---
## Strategic Outlook
Both deposit and loan portfolios show **high-value client concentration** and **European regional dominance**.  
The current structure offers **stability and low default risk**, but limited growth scalability.  
Diversification across **income tiers, occupations, and geographies** will be essential for balanced, long-term expansion.

---



