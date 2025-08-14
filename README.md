# LinkedIn Job Market Analysis

## Motivation
This process is just a result of the desire to apply my learnings during my masters towards solving one of my problems. Like most job seekers I spend a lot of time on LinkedIn wondering why some jobs get hundreds of applicants while others barely get noticed. I wanted to understand what actually drives applications so I could use that insight for my own search and share it with others.

## Project Overview
I collected data from over twenty thousand LinkedIn job postings by scraping the platform and structured it for analysis. The dataset included information such as job title, location, remote work options, sponsorship, pay type, salary range, number of views and applications, skills, work type, and company information.

The analysis was done in multiple stages:  
1. **Data Cleaning and Preprocessing** – Removed redundancies, handled missing values, and ensured data quality.  
2. **Exploratory Data Analysis (EDA)** – Looked at distributions of jobs by state, country, work type, company, salary range, and top skills in different locations.  
3. **Statistical Modeling** – Applied Multiple Linear Regression (OLS) to quantify how different job attributes affect the number of applications. Checked assumptions such as linearity, no perfect collinearity, zero conditional mean, and normality of residuals. Adjusted for heteroscedasticity using White’s robust standard errors.  
4. **Machine Learning Models** – Compared Linear Regression, Lasso Regression, Decision Tree, Random Forest, and SVR for predictive performance. Linear Regression had the highest R² and balanced accuracy with interpretability.

## Statistical Analysis Highlights
**Model Specification:**  

log(Applications) = β0
+ β1·log(Views)
+ β2·OffsiteApply
+ β3·RemoteAllowed
+ β4·Sponsored
+ β5·ContractWork
+ β6·HourlyPay
+ β7·MidwestLocation
+ β8·ComplexOnsiteApply
+ β9·SimpleOnsiteApply
+ β10·CentralPlainsLocation
+ β11·NortheastLocation
+ β12·SouthLocation 

**Key Results:**  
- 1% increase in views → 0.92% increase in applications.  
- Remote work → +25.77% applications.  
- Hourly pay → +14.27% applications.  
- Offsite apply → –65% applications.  
- Complex onsite apply → –27.54% applications.  
- Sponsorship → –10.08% applications.  
- Location matters — some regions see significantly more or fewer applications.

## Key Insights
- Visibility is important, but the application process strongly impacts applicant numbers.  
- Flexibility in work arrangement and pay attracts more candidates.  
- Certain geographic regions are inherently more competitive.

## Tech Stack
- Python  
- Pandas, NumPy, Matplotlib, Seaborn  
- Statsmodels, Scikit-learn  
- Jupyter Notebook

## How to Use
Open `Linkedin_Job_Analysis.ipynb` to explore the analysis and models.  
Dataset is not included due to size — can be recreated by scraping LinkedIn job postings.



