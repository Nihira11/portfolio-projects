# Portfolio Projects

# Data Analytics / Data Science Portfolio

Hi, I’m Nihira. This portfolio showcases my projects in data analytics, dashboards, machine learning, statistical inference and web-based data apps, across Power BI, Python/Streamlit, R/Shiny, SQL/PostgreSQL and Tableau.

## Projects

### 1. Netflix Dashboard
Power BI dashboard analysing Netflix titles, genres, countries, and release trends.

- Tools: Power BI, Excel/CSV
- Repo: [Netflix Dashboard](https://github.com/Nihira11/netflix-dashboard)
- Dashboard screenshot: ![Overview](https://github.com/Nihira11/netflix-dashboard/blob/main/netflix-content-analysis/screenshots/dashboard_overview.png)

Highlights:
1. Catalogue split across Movies (71%) and TV Shows (29%), with genre, rating and country breakdowns
2. Power Query cleaning (date parsing, splitting multi-value country/genre fields) and DAX measures (Total Titles, Peak Content Year)
3. Cross-filtering across KPI cards, donut, genre bars, a content-growth area chart and a world map
4. Insights: content additions peaked in 2019; the US leads volume (then India); Dramas and International content dominate; South Korea skews TV-heavy
---

### 2. Automated EDA Tool
A Streamlit web app that automatically generates dataset summaries, missing value analysis, distributions, correlations and outlier insights.

- Tools: Python, Streamlit, Pandas, Plotly, Matplotlib
- Repo: [Automated EDA Tool](https://github.com/Nihira11/automated-eda-tool)
- Live App: [Open Dashboard](https://automated-eda-tool.streamlit.app/)
- App screenshot: ![Overview](https://github.com/Nihira11/automated-eda-tool/blob/main/screenshots/overview.png)

Highlights:
1. Upload any CSV and get an instant overview, automated insights and data-quality warnings
2. Missing-value analysis, IQR-based outlier detection, distribution + skewness checks and correlation heatmaps
3. Automatic target-variable analysis with driver ranking and feature-importance insights
4. Duplicate, high-cardinality and ID-column detection; modular modules/ design; tested on the Telco and Titanic datasets

---

### 3. Customer Churn Prediction & Retention Dashboard
An end-to-end churn prediction and retention analytics dashboard that scores customers, explains predictions and quantifies revenue exposure.

- Tools: Python, Streamlit, Pandas, Scikit-learn, XGBoost, SHAP, Plotly
- Repo: [Customer Churn Project](https://github.com/Nihira11/telco-churn-retention-app)
- Live App: [Open Dashboard](https://bank-churn-intel.streamlit.app/)
- App/Dashboard: ![Overview](https://github.com/Nihira11/bank-churn-intelligence/blob/main/screenshots/01_overview_kpi.png)

Highlights:
1. XGBoost final model (ROC-AUC 0.875) selected over Logistic Regression and Random Forest
2. Live SHAP waterfall explainability for any customer profile in the Prediction Centre
3. K-Means segmentation (k=4) into churn-risk personas, plus a revenue-at-risk framework (~$105.9M total exposure)
4. Retention Centre with a threshold-filtered at-risk list and CSV export
5. Caught and removed a data-leakage feature (Complain) that had inflated metrics to ~1.0 ROC-AUC; 10,000 customers, 20.38% churn rate

---

### 4. A/B Testing + Decision Analysis Dashboard

A Streamlit experimentation dashboard that combines frequentist A/B testing, Bayesian inference, power analysis, revenue impact modelling, and automated PDF reporting to support launch decisions.

- Tools: Python, Streamlit, Pandas, NumPy, SciPy, Statsmodels, Plotly, ReportLab
- Repo: [A/B Testing Decision Dashboard](https://github.com/Nihira11/ab-testing-decision-dashboard)
- Live App: [Open Dashboard](https://ab-testing-decision-dashboard.streamlit.app/)
- Dashboard screenshot: ![Overview](https://github.com/Nihira11/ab-testing-decision-dashboard/blob/main/screenshots/01_home_dashboard.png)

Highlights:
1. Frequentist (two-proportion z-test, confidence intervals, power, MDE) and Bayesian (Beta-Binomial posterior, P(treatment better), expected loss) engines side by side
2. Sample Ratio Mismatch (SRM) health checks before analysis, plus a Decision Centre that turns statistics into ship / don’t-ship calls with revenue-impact projections
3. Validated on the public Udacity e-commerce dataset (294,000+ observations) – correctly returned a DO NOT SHIP recommendation
4. Stakeholder-ready PDF and Markdown report export

---

### 5. Stock Trend Analysis & Volatility Insights

An interactive R/Shiny dashboard for equity trend, risk and volatility analysis. It pulls live daily prices from Yahoo Finance, computes the indicators and risk statistics a desk analyst actually uses and fits a family of GARCH models to quantify and forecast volatility, including the leverage effect that makes downside shocks hit harder than upside ones.

- Tools: R, Shiny (bslib), tidyquant, TTR, PerformanceAnalytics, rugarch, plotly, zoo, memoise, testthat
- Repo: [Stock Trend & Volatility](https://github.com/Nihira11/stock-trend-volatility)
- Live App: [Open Dashbaord](https://nihirasharma.shinyapps.io/stock-trend-volatility/)
- Dashboard screenshot: ![Overview](https://github.com/Nihira11/stock-trend-volatility/blob/main/screenshots/overview.png?raw=true)

Highlights:
1. GARCH family (sGARCH / eGARCH / gjrGARCH) with model selection by BIC, a news-impact curve for the asymmetry and 10–60 day volatility forecasts
2. Value-at-Risk and CVaR (Expected Shortfall) with Kupiec proportion-of-failures backtesting and an ARCH-LM pre-test for volatility clustering
3. Out-of-sample 80/20 train–test validation of GARCH forecasts against a constant-volatility benchmark
4. Five pages – Overview, Trends (SMA crossovers, RSI, MACD, Bollinger), Risk (VaR/CVaR, drawdown), Volatility (GARCH) and multi-ticker Compare
5. Works on US tickers, indices (^GSPC), and ASX names (CBA.AX); two-layer RDS + memoised caching for instant reloads
6. All risk/volatility maths in pure, reusable R functions under R/, covered by testthat unit tests against hand-computed values

---

### 6. Fraud Risk Intelligence Platform

A SQL-first fraud detection and risk-scoring pipeline. Feature engineering is done entirely in PostgreSQL, an XGBoost model is benchmarked against a transparent SQL rule engine and every transaction is ranked into an expected-loss alert queue served through a live, single-screen dashboard.

- Tools: PostgreSQL, Python, Pandas, Scikit-learn, XGBoost, LightGBM, SQL, Plotly.js, Tableau
- Repo: [Fraud Risk Intelligence Platform](https://github.com/Nihira11/fraud-risk-intelligence-platform)
- Live Dashboard: [Open Dashboard](https://nihira11.github.io/fraud-risk-intelligence-platform/dashboard/)
- Tableau Public: [Open Dashboard](https://public.tableau.com/app/profile/nihira.sharma/viz/FraudRiskIntelligencePlatform/Fraud_Risk_Intelligence?publish=yes)
- Dashboard screenshot: ![Overview](https://github.com/Nihira11/fraud-risk-intelligence-platform/blob/main/screenshots/dashboard_main.png)

Highlights:
1. SQL-first design: per-card amount z-scores, trailing-window velocity counts and haversine distances engineered as a PostgreSQL materialized view, with Python used only for the ML layer
2. XGBoost final model (PR-AUC 0.883) selected from a five-model bake-off (vs LightGBM, Random Forest, Logistic Regression, Isolation Forest) on a time-based train/test split; lifts precision from the rule engine's 17% to 99.2% at equal recall
3. Expected-loss ranking (P(fraud) × amount) turns scores into a capacity-aware review queue: reviewing the top 1,000 of 2,730 alerts catches 75% of all fraud and recovers ~$529K (85%) of fraud-dollar exposure
4. Honest negative result documented: engineered geo-distance and impossible-travel features carry no signal because the Sparkov dataset's coordinates are synthetic
5. Two dashboards from one pipeline: a custom HTML/CSS/JS single-screen risk console (Plotly.js, GitHub Pages) and a Tableau Public BI dashboard, plus EDA and model-development notebooks
6. 1.3M transactions, 0.58% fraud rate; synthetic-data caveat stated throughout so the ~99% precision is read in context

---

## Skills Demonstrated

- **Languages & tools:** Python, R, SQL (PostgreSQL), Power BI, Tableau, Git
- **Machine learning:** classification (XGBoost, Random Forest, Logistic Regression), model explainability (SHAP), out-of-sample validation
- **Statistics & experimentation:** A/B testing, Bayesian inference, hypothesis testing, power analysis
- **Time-series & quant:** volatility modelling (GARCH family), Value-at-Risk & Expected Shortfall, risk backtesting (Kupiec, ARCH-LM)
- **Data engineering:** SQL feature engineering (materialized views, window functions), EDA, data cleaning
- **Analytics & delivery:** dashboard development (Streamlit, Shiny, Power BI, Tableau), business insight generation, decision/expected-loss analysis

## Contact

- GitHub: [GitHub link](https://github.com/Nihira11)
- LinkedIn: [LinkedIn link](https://www.linkedin.com/in/nihira-sharma-608b97296/)
