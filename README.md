# Banking Dashboard Analysis

## Problem Statement
Develop a basic understanding of risk analytics in banking and financial services and understand how data is used to minimise the risk of losing money while lending to customers.

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

## Tools and Techniques
- **Power BI**
- **DAX (Data Analysis Expressions)**
- **Data Modeling**
- **Business Intelligence Visualization**

---



