# Portfolio Projects

Hi, I’m Nihira Sharma. This portfolio includes my projects in data analytics, machine learning, statistics, risk modelling and interactive dashboard development. The projects use tools such as Python, R, SQL, PostgreSQL, Power BI, Tableau, Streamlit and Shiny.

## Projects

### 1. Fraud Risk Intelligence Platform

A complete fraud detection platform that scores credit-card transactions and helps investigators decide which alerts to review first. Features are created in PostgreSQL, while an XGBoost model predicts fraud risk. Alerts are ranked by expected financial loss and displayed in an interactive investigation dashboard.

- Tools: PostgreSQL, Python, Pandas, Scikit-learn, XGBoost, LightGBM, SQL, Plotly.js, Tableau
- Repo: [Fraud Risk Intelligence Platform](https://github.com/Nihira11/fraud-risk-intelligence-platform)
- Live Dashboard: [Open Dashboard](https://nihira11.github.io/fraud-risk-intelligence-platform/dashboard/)
- Tableau Public: [Open Dashboard](https://public.tableau.com/app/profile/nihira.sharma/viz/FraudRiskIntelligencePlatform/Fraud_Risk_Intelligence?publish=yes)
- Dashboard screenshot: ![Overview](https://github.com/Nihira11/fraud-risk-intelligence-platform/blob/main/screenshots/dashboard_main.png)

**Highlights:**
1. Ranks transactions using expected loss:
   ```
   Expected Loss = Probability of Fraud × Transaction Amount
   ```
   Reviewing the top 1,000 of 2,730 alerts finds 75% of all fraud cases and covers approximately $529,000, or 85% of the total fraud-dollar exposure
2. Compared several machine learning models using a time-based train and test split. XGBoost achieved a PR-AUC of 0.883
3. At the same recall level, XGBoost achieved 99.2% precision, compared with 53.5% for Logistic Regression and 17% for the SQL rule engine
4. Features such as card-level spending z-scores, recent transaction counts, and geographic distances were created inside PostgreSQL
5. Geographic distance and impossible-travel features were tested but removed because the synthetic merchant locations did not contain useful information
6. Includes a custom HTML and JavaScript investigation dashboard, a Tableau Public dashboard and notebooks for data analysis and model development
7. Uses 1.3 million synthetic transactions with a fraud rate of 0.58%. The synthetic-data limitation is clearly explained throughout the project

---

### 2. Credit Risk Intelligence Platform

A complete credit scoring platform built using the Home Credit Default Risk dataset. PostgreSQL combines more than 58 million records from seven tables. Logistic Regression and XGBoost models are compared and the selected model is converted into an explainable credit scorecard.

- Tools: R, PostgreSQL, Shiny (bslib), scorecard, XGBoost, `glm`, `caret`, tidyverse, `testthat`
- Repo: [Credit Risk Intelligence Platform](https://github.com/Nihira11/credit-risk-intelligence-platform)
- Live Dashboard: [Open Dashboard](https://nihirasharma.shinyapps.io/credit-risk-intelligence-platform/)
- Notebooks (GitHub Pages): [Model Development](https://nihira11.github.io/credit-risk-intelligence-platform/notebooks/03_modeling.html)
- Dashboard screenshot: ![Overview](https://github.com/Nihira11/credit-risk-intelligence-platform/blob/main/screenshots/dashboard_performance.png) ![Overview Table](https://github.com/Nihira11/credit-risk-intelligence-platform/blob/main/screenshots/performance_table.png) 

**Highlights:**
1. Combined more than 58 million records from seven tables into an analytics dataset containing 307,511 applicants
2. Used Weight of Evidence and Information Value to prepare and select useful credit risk features
3. Selected a 16-feature Logistic Regression model instead of XGBoost because it was easier to explain and more suitable for a credit scorecard
4. Found and removed six strongly related count features that caused missing model coefficients
5. The final scorecard closely reproduced the model, with a Gini difference of approximately 0.00007
6. The final model achieved:
   - AUC: 0.66
   - Gini: 0.31
   - KS: 0.23
7. Created approval, review and decline groups. The system automatically approved 22% of applicants with a 3.6% default rate, compared with an overall default rate of 8.1%
8. Tested calibration, population stability and fairness across gender and age groups
9. Includes a four-page Shiny dashboard and 28 automated tests

---

### 3. Customer Churn Prediction & Retention Dashboard (Bank Churn Intelligence)
A customer churn prediction and retention platform that identifies customers who may leave the bank, explains each prediction and estimates the revenue at risk.

- Tools: Python, Streamlit, Pandas, Scikit-learn, XGBoost, SHAP, Plotly
- Repo: [Customer Churn Project](https://github.com/Nihira11/telco-churn-retention-app)
- Live App: [Open Dashboard](https://bank-churn-intel.streamlit.app/)
- App/Dashboard: ![Overview](https://github.com/Nihira11/bank-churn-intelligence/blob/main/screenshots/01_overview_kpi.png)

**Highlights:**
1. Compared Logistic Regression, Random Forest and XGBoost
2. Selected XGBoost as the final model with a ROC-AUC score of 0.875
3. Uses live SHAP waterfall charts to explain why an individual customer received a certain churn probability
4. Divides customers into four groups using K-Means clustering
5. Estimates approximately $105.9 million in total revenue at risk
6. Includes a Retention Centre with customer filters, risk thresholds and CSV downloads
7. Found and removed the Complain feature because it caused data leakage and increased ROC-AUC to an unrealistic score of approximately 1.0
8. Uses 10,000 customer records with an overall churn rate of 20.38%

---

### 4. A/B Testing + Decision Analysis Dashboard

An interactive A/B testing dashboard that helps teams decide whether a product change should be launched. It combines Frequentist and Bayesian analysis, measures business risk, estimates revenue impact and gives one of three recommendations: **Ship, Continue Testing or Do Not Ship**


- Tools: Python, Streamlit, Pandas, NumPy, SciPy, Statsmodels, Plotly, ReportLab
- Repo: [A/B Testing Decision Dashboard](https://github.com/Nihira11/ab-testing-decision-dashboard)
- Live App: [Open Dashboard](https://ab-testing-decision-dashboard.streamlit.app/)
- Dashboard screenshot: ![Overview](https://github.com/Nihira11/ab-testing-decision-dashboard/blob/main/screenshots/01_home_dashboard.png)

**Highlights:**
1. Tested using the public Udacity E-Commerce A/B Testing dataset, which contains more than 294,000 user records
2. Correctly found that the treatment performed worse than the control and produced a DO NOT SHIP recommendation
3. Includes Frequentist methods such as:
   - Two-proportion z-test
   - Confidence intervals
   - Power analysis
   - Minimum Detectable Effect
4. Includes Bayesian methods such as:
   - Beta-Binomial modelling
   - Probability that treatment is better
   - Expected improvement
   - Expected loss
5. Checks for Sample Ratio Mismatch (SRM) before analysing an experiment
6. Converts statistical results into business recommendations and revenue estimates
7. Automatically creates PDF and Markdown reports for stakeholders

---

### 5. Stock Trend Analysis & Volatility Insights

An interactive R/Shiny dashboard for studying stock prices, trends, risk and volatility. The app downloads daily market data from Yahoo Finance, calculates technical indicators and risk measures and uses GARCH models to forecast volatility.

- Tools: R, Shiny (bslib), tidyquant, TTR, PerformanceAnalytics, rugarch, plotly, zoo, memoise, `testthat`
- Repo: [Stock Trend & Volatility](https://github.com/Nihira11/stock-trend-volatility)
- Live App: [Open Dashbaord](https://nihirasharma.shinyapps.io/stock-trend-volatility/)
- Dashboard screenshot: ![Overview](https://github.com/Nihira11/stock-trend-volatility/blob/main/screenshots/overview.png?raw=true)

**Highlights:**
1. Compares sGARCH, eGARCH, and gjrGARCH models and selects the best model using BIC
2. Creates volatility forecasts for periods between 10 and 60 days
3. Calculates Value at Risk and Conditional Value at Risk
4. Uses the Kupiec test to check whether VaR is breached as often as expected
5. Uses an ARCH-LM test to check whether volatility clustering is present before fitting GARCH models
6. Tests forecasts using an 80/20 train and test split and compares them with a constant-volatility model
7. Includes five dashboard pages:
   - Overview
   - Trends
   - Risk
   - Volatility
   - Multi-ticker comparison
8. Supports US stocks, market indices such as `^GSPC` and Australian stocks such as `CBA.AX`
9. Stores downloaded prices and model results to make repeat analysis faster
10. Keeps the financial calculations in reusable R functions with automated tests

---

### 6. Automated EDA Tool
An interactive Streamlit app that automatically analyses uploaded CSV files. It creates dataset summaries, finds missing values and outliers, studies distributions and correlations, and produces automatic insights without requiring code.

- Tools: Python, Streamlit, Pandas, Plotly, Matplotlib
- Repo: [Automated EDA Tool](https://github.com/Nihira11/automated-eda-tool)
- Live App: [Open Dashboard](https://automated-eda-tool.streamlit.app/)
- App screenshot: ![Overview](https://github.com/Nihira11/automated-eda-tool/blob/main/screenshots/overview.png)

**Highlights:**
1. Upload any CSV file and receive an instant dataset overview
2. Automatically identifies:
   - Missing values
   - Possible outliers
   - Skewed columns
   - Strong correlations
   - Duplicate records
   - High-cardinality columns
   - Possible ID columns
3. Uses the IQR method to detect outliers
4. Allows users to select a target variable and view its most important drivers
5. Uses separate Python modules for each analysis page
6. Tested using the Telco Customer Churn and Titanic datasets

---

### 7. Netflix Dashboard
A Power BI dashboard that analyses Netflix movies and television shows by genre, country, rating, and release year.

- Tools: Power BI, Power Query, DAX, Excel, CSV
- Repo: [Netflix Dashboard](https://github.com/Nihira11/netflix-dashboard)
- Dashboard screenshot: ![Overview](https://github.com/Nihira11/netflix-dashboard/blob/main/netflix-content-analysis/screenshots/dashboard_overview.png)

**Highlights:**
1. Shows that the Netflix catalogue contains approximately:
   - 71% movies
   - 29% television shows
2. Uses Power Query to clean dates and separate columns containing multiple countries or genres
3. Uses DAX to calculate measures such as Total Titles and Peak Content Year
4. Includes interactive filters across KPI cards, charts, and a world map
5. Main findings include:
   - Content additions reached their highest level in 2019
   - The United States has the most titles, followed by India
   - Drama and international content are the largest categories
   - South Korea has a higher share of television content

---

## Skills Demonstrated

- **Languages & Querying:** Python, R, SQL/PostgreSQL
- **Machine Learning:** XGBoost, LightGBM, Logistic Regression, Random Forest, Isolation Forest, K-Means clustering, SHAP explainability, feature engineering (WOE/IV, z-scores), data leakage detection
- **Risk & Statistics:** Credit scorecard modelling, GARCH volatility forecasting, VaR/CVaR, Frequentist & Bayesian A/B testing, hypothesis testing, backtesting (Kupiec, ARCH-LM)
- **Data Engineering:** Large-scale SQL feature pipelines (1M–58M+ records), automated EDA, outlier/missing-value detection
- **Dashboards & BI:** Streamlit, Shiny, Power BI, Tableau, Plotly
- **Software Practices:** Automated testing, modular code, reproducible notebooks, version control (Git/GitHub)
- **Business Impact:** Translating models into financial metrics (expected loss, revenue at risk) and stakeholder-ready recommendations

## Contact

- GitHub: [GitHub link](https://github.com/Nihira11)
- LinkedIn: [LinkedIn link](https://www.linkedin.com/in/nihira-sharma-608b97296/)
