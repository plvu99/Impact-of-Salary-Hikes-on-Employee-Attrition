# Impact of Salary Hikes on Employee Attrition

## 🔎 Overview

Employee turnover is one of the most expensive operational challenges organizations face. High attrition leads to lost institutional knowledge, decreased productivity, and increased recruitment costs. In the United States alone, businesses lose nearly $1 trillion annually due to employee departures, and replacing a single employee can cost 50–200% of their annual salary. 

This project investigates **whether increasing employee salaries significantly reduces attrition rates**. Using HR analytics data, the analysis examines salary increases alongside other factors such as job satisfaction, work-life balance, and career progression to determine what truly drives employee retention.

## 🔐 Business Problem

Many organizations attempt to retain talent primarily through salary increases. However, compensation may not be the sole driver of employee loyalty.

Companies must answer an important question: _Does increasing salary meaningfully reduce employee attrition?_

If salary increases alone are insufficient, organizations risk allocating retention budgets inefficiently. Understanding the real drivers of attrition allows HR leaders to design more effective retention strategies that focus on:
- Employee engagement
- Career development
- Workplace culture
- Long-term incentives

This study focuses on technology and consulting roles, where competition for skilled talent is particularly intense.

## 📊 Dataset

The analysis uses the IBM HR Analytics Employee Attrition & Performance dataset available on [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset/data).

The dataset includes employee information across several dimensions:

**Employee attributes**
- Age
- Department
- Job level
- Years at company

**Compensation metrics**
- Monthly income
- Percentage salary hike
- Stock option level

**Work environment variables**
- Job satisfaction
- Work-life balance
- Performance rating

**Outcome variable**
- Attrition status (whether an employee left the company)

In this study:
- **Independent variable:** Percentage Salary Hike
- **Dependent variable:** Employee Attrition

Several additional variables were included as confounding factors to control for other drivers of employee turnover.

## 📍 Methodology

The analysis combines descriptive analytics and causal inference techniques.

### 1. Data Cleaning and Filtering

Several preprocessing steps were applied:
- Removed employees without salary hikes
- Dropped rows with missing key variables
- Removed extreme salary hike outliers
- Excluded records with inconsistent promotion data
- Filtered employees with invalid tenure values

These steps ensured a clean dataset for causal analysis.

### 2. Exploratory Data Analysis

Initial analysis explored salary distributions and attrition patterns.

Key observations:
- Most salary increases fall between 10–20%
- Salary hike distributions are similar for employees who stayed vs. left
- Attrition patterns vary more strongly with job satisfaction and tenure than with salary changes. 

### 3. Logistic Regression

A logistic regression model was used to estimate the probability of attrition:

```
Attrition = f(SalaryHike, JobSatisfaction, WorkLifeBalance, YearsAtCompany, StockOptions, JobLevel)
```

This approach evaluates how each factor influences the likelihood of employee turnover.

### 4. Difference-in-Differences (DiD)

To estimate the causal impact of salary hikes, the study used a Difference-in-Differences (DiD) approach.

- **Treatment group:** Employees receiving salary hikes greater than 18%
- **Control group:** Employees receiving salary hikes below 18%
- **Pre-treatment period:** Employees promoted within the past two years
- **Post-treatment period:** Employees promoted earlier than two years

<img width="584" height="455" alt="image" src="https://github.com/user-attachments/assets/57d20ba2-93d1-4cb4-ae58-91bffb6ee9c2" />

<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/4b3afeb0-bc29-4b4c-958b-20e3597cb515" />

The DiD regression model isolates the effect of salary increases while controlling for other external factors.

## 🔑 Key Insights

### 1. Salary hikes have weak impact on attrition

Salary increases show very weak correlation with employee attrition.

The logistic regression model indicates that salary hikes are not statistically significant predictors of employee turnover.

### 2. Employee satisfaction is a strong retention driver

Two variables significantly reduce attrition risk:
- Job satisfaction
- Work-life balance

Employees who feel engaged and supported in their roles are much more likely to remain with the organization.

### 3. Career growth and long-term incentives matter

The analysis shows strong retention effects for:
- Stock options
- Job level progression
- Longer tenure

Employees who see long-term growth opportunities are less likely to leave.

### 4. Salary alone cannot solve retention problems

The Difference-in-Differences analysis confirms that even significant salary increases do not meaningfully change attrition rates.

Retention is driven by a combination of engagement, career development, and workplace satisfaction rather than compensation alone. 

## ✍️ Business Recommendations

### 1. Focus on employee engagement

Invest in improving job satisfaction through meaningful work, recognition programs, and strong leadership.

### 2. Improve work-life balance

Organizations should implement policies that support employee well-being, such as flexible work arrangements, manageable workloads, and mental health support.

### 3. Create clear career development paths

Employees remain longer when they see opportunities for growth. Companies should prioritize mentorship programs, promotion transparency, and skill development initiatives.

### 4. Use compensation strategically

Salary increases should be part of a broader retention strategy, combined with stock options, performance incentives, and long-term rewards.

## ⚙ Tools & Techniques

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Statistical Modeling (Logistic Regression, Difference-in-Differences)
