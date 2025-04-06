# 📉 Impact of Salary Hikes on Employee Attrition

## 📋 Overview

### Problem Statement
Employee turnover is expensive. In the US, businesses lose nearly **$1 trillion annually** due to employee departures (Gallup, 2019). Replacing an employee can cost **between 50% and 200% of their annual salary** (SHRM, 2022). This doesn’t just impact finances; it also leads to lost talent and productivity drop. Therefore, companies need to understand the factors driving attrition and improve their retention strategies.

### Research Question
_**Does significantly increasing salary have an effect on employee attrition?**_

Salary is a tangible, universally comparable measure, and it often guides employees’ decisions to stay or leave. We also examine other factors, including job satisfaction, work-life balance, years at company, and so on, to have a better understanding.

Our study focuses on **Tech and Consulting** industries, which are both highly competitive and talent-driven. Salary hikes are crucial for retaining top talent in these fields.

Our data is all **voluntary** and **US-based only**, from **R&D, HR, and Sales departments**. These roles require specialized skills and face intense competition, so competitive pay is essential for loyalty.

Through this analysis, we aim to provide actionable insights to help companies enhance their retention strategies.

### Initial Descriptive Statistics and Visualizations
- Most salary hikes fall between 10-20%, indicating a structured salary raise policy.
- There is no major difference in salary hike distribution between employees who stayed vs. left.
- Salary hikes alone do not strongly influence attrition—other factors like job satisfaction and career growth matter more.

### Multiple Possible Outcomes
- Higher salary hike reduces attrition (Google, Costco).
- There is no significant relationship between salary hikes and attrition (Goldman Sachs, McKinsey & Company).
- Higher salary hike increases attrition (Goldman Sachs, Citibank, J.P.Morgan).

## 📊 Analysis

### Data Overview
The dataset was from Kaggle: [IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset/data)

**Key Variables:**
- X (Independent Variable): Percentage Salary Hike
- Y (Dependent Variable): Attrition Rate

**Confounding Variables:**
- Job Satisfaction
- Work-life Balance
- Years at Company
- Stock Options
- Job Level

### Proposed Ideal Experiment
- **Logistic Regression**
- **Difference-in-Differences (DiD):**
  - Mimics an experiment using real-world salary hike data.
  - Leverages natural salary increases as the ‘treatment’ while keeping a control group.
  - Removes bias from factors affecting both groups equally (e.g., economy, company policies).

## 📝 Conclusion
_Retention isn’t just about compensation—it’s about commitment!_
- There is strong evidence that significant salary hikes alone do not guarantee employee retention.
- Investing in employee satisfaction, career development, and a supportive work environment will yield better long-term retention!
