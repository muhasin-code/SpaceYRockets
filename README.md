# 🚀 SpaceX Falcon 9 Launch Success Analysis

## 📌 Project Overview
This project is an end-to-end **data science capstone** that analyzes **SpaceX Falcon 9 launch data** to understand the key factors influencing launch success.  
The study combines **data collection, exploratory data analysis, interactive visualization, SQL analytics, and machine learning classification** to derive actionable insights.

The goal is to determine:
- What factors affect launch success?
- How payload, orbit, launch site, and booster version influence outcomes?
- Whether launch success can be predicted using machine learning models.

---

## 🧠 Key Objectives
- Collect launch data from multiple sources (APIs and web scraping)
- Perform data cleaning and feature engineering
- Conduct exploratory data analysis using Python and SQL
- Build interactive maps and dashboards
- Train and evaluate classification models to predict launch success


---

## 🛠️ Tools & Technologies Used

### Programming & Libraries
- **Python** (Pandas, NumPy, Matplotlib, Seaborn)
- **Scikit-learn** (Logistic Regression, SVM, Decision Tree)
- **BeautifulSoup** (Web Scraping)
- **Requests** (API calls)

### Data & Analytics
- **SpaceX REST APIs**
- **SQL (SQLite / Pandas SQL interface)**

### Visualization & Interaction
- **Folium** – Interactive geospatial maps
- **Plotly Dash** – Interactive dashboard

---

## 🔗 Data Collection

### 1. SpaceX REST APIs
Data was retrieved from multiple SpaceX API endpoints:
- Launches
- Rockets
- Payloads
- Launchpads

These datasets were merged to create a comprehensive launch-level dataset.

### 2. Web Scraping
Historical launch records were scraped from Wikipedia using **BeautifulSoup** and structured into tabular format.

---

## 🧹 Data Wrangling
- Removed missing and inconsistent values
- Converted categorical variables into numerical format
- Engineered new features such as:
  - Launch year
  - Success class (1 = success, 0 = failure)

---

## 📊 Exploratory Data Analysis (EDA)

### Visual Analysis
- Payload Mass vs Launch Outcome
- Orbit Type vs Success Rate
- Launch Site vs Success Rate
- Yearly Success Trend

### SQL Analysis
- Unique launch sites
- Total and average payload mass
- Landing outcome frequencies
- Booster performance analysis

---

## 🌍 Interactive Visual Analytics

### Folium Map
- Launch site locations plotted globally
- Success and failure outcomes visualized using markers
- Distance analysis to coastlines, highways, and railways

📌 Notebook: `06_interactive_map_folium.ipynb`

---

## 📈 Interactive Dashboard (Plotly Dash)
The dashboard allows:
- Selection of launch sites via dropdown
- Payload filtering using a range slider
- Visualization of:
  - Launch success count
  - Site-specific success ratio
  - Payload vs outcome scatter plot

📌 File: `dashboard/spacex_dash_app.py`

---

## 🤖 Predictive Analysis (Machine Learning)

### Models Built
- Logistic Regression
- Support Vector Machine (SVM)
- Decision Tree

### Model Evaluation
- Accuracy score
- Confusion matrix
- Cross-validation
- Hyperparameter tuning using GridSearchCV

### Best Model
- **Support Vector Machine (SVM)** achieved the highest classification accuracy
- Demonstrated excellent recall for successful launches

---

## 📌 Key Findings
- Launch success rate improves significantly over time
- Medium payload ranges (~3000–6000 kg) have the highest success rates
- Falcon 9 Block 5 boosters outperform earlier versions
- KSC LC-39A is the most reliable launch site
- Machine learning models can effectively predict launch outcomes

---

## 📄 Final Presentation
The final project presentation is available in PDF format:

📎 `presentation/spacex_capstone_presentation.pdf`

---

## 🚀 How to Run the Project

### Run Dash App
```bash
python dashboard/spacex_dash_app.py
