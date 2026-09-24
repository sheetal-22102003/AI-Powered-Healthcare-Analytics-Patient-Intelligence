# 🏥 HEALTHCARE INSIGHT360
## AI-Powered Healthcare Analytics & Patient Intelligence Dashboard

> **"Transforming Healthcare Data into Actionable Patient, Operational & Clinical Insights"**

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-red?style=flat-square&logo=streamlit)
![Plotly](https://img.shields.io/badge/Plotly-5.15+-blueviolet?style=flat-square&logo=plotly)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-orange?style=flat-square&logo=scikit-learn)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

## 📋 Project Overview

**Healthcare Insight360** is a complete, industry-grade healthcare data analytics system built using Python, Pandas, Scikit-learn, Plotly, and Streamlit. It transforms raw patient admission data into actionable insights across patient demographics, clinical patterns, hospital operations, financials, and predictive risk analytics.

The project includes:
- Complete exploratory data analysis (EDA)
- 17+ healthcare KPIs computed automatically
- K-Means patient segmentation
- Time-series admission and revenue trend analysis
- Machine learning readmission risk prediction (Logistic Regression, Decision Tree, Random Forest, Gradient Boosting)
- A fully interactive 7-page Streamlit dashboard with filters, charts, and download options

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 📊 Executive Overview | KPI cards, trend charts, demographic breakdowns |
| 👥 Patient Analytics | Age, gender, blood type, insurance, segmentation |
| 🩺 Clinical Analytics | Conditions, medications, test results, LOS |
| 🏥 Hospital Operations | Workload, admissions heatmap, LOS analysis |
| 💰 Financial Analytics | Revenue trends, billing by category, insurance analysis |
| 🤖 Predictive Analytics | Readmission prediction, model comparison, feature importance |
| 💡 Insights Engine | Auto-generated textual insights + strategic recommendations |

---

## 📁 Project Structure

```
HEALTHCARE_INSIGHT360/
│
├── data/
│   └── healthcare_dataset.csv          ← Source dataset (synthetic/anonymized)
│
├── notebooks/
│   └──Sheetal_HealthcareInsight360.ipynb  ← Full analysis notebook
│
├── dashboard/
│   ├── app.py                          ← Main Streamlit dashboard
│   ├── components.py                   ← Reusable Plotly chart components
│   └── utils.py                        ← Data loading, KPI & insight utilities
│
├── models/
│   └── readmission_model.pkl           ← Saved best ML model (auto-generated)
│
├── outputs/
│   ├── charts/                         ← Saved chart images (from notebook)
│   ├── cleaned_data/                   ← Cleaned dataset CSV (from notebook)
│   └── reports/                        ← KPI summary CSV, insights TXT
│
├── requirements.txt                    ← Python dependencies
├── README.md                           ← This file
└──Sheetal _HealthcareInsight360_ProjectReport.docx  ← Project report
```

---

## 📦 Dataset

| Property | Detail |
|---|---|
| **Dataset Name** | healthcare_dataset.csv |
| **Type** | Synthetic / Anonymized |
| **Records** | ~10,000 patient records |
| **Source** | [Kaggle Healthcare Dataset](https://www.kaggle.com/datasets/prasad22/healthcare-dataset) |
| **Columns** | Name, Age, Gender, Blood Type, Medical Condition, Date of Admission, Doctor, Hospital, Insurance Provider, Billing Amount, Room Number, Admission Type, Discharge Date, Medication, Test Results |

> ⚠️ This dataset is **synthetic and anonymized**. It does not represent real patient records. No real patient data is used in this project.

---

## 🔧 Technologies Used

| Category | Tools |
|---|---|
| **Language** | Python 3.10+ |
| **Data Manipulation** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn, Plotly |
| **Machine Learning** | Scikit-learn |
| **Dashboard** | Streamlit |
| **Model Serialization** | Joblib |
| **Notebook** | Jupyter |
| **Report** | Python-docx |

---

## 🚀 Installation & Setup

### 1. Prerequisites

- Python 3.10 or higher
- pip (Python package manager)

### 2. Clone / Download the Project

```bash
# If using Git
git clone https://github.com/yourusername/healthcare-insight360.git
cd healthcare-insight360/HEALTHCARE_INSIGHT360

# Or navigate to the project folder
cd HEALTHCARE_INSIGHT360
```

### 3. Create a Virtual Environment (Recommended)

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python -m venv venv
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

### Option A: Run the Jupyter Notebook

```bash
cd notebooks
jupyter notebook MansiKushwaha_HealthcareInsight360.ipynb
```

This runs all 8 parts:
- Data Loading → Data Cleaning → EDA → KPI Engine → Advanced Analytics → ML → Insights → Export

### Option B: Run the Streamlit Dashboard

```bash
streamlit run dashboard/app.py
```

Then open your browser at: **http://localhost:8501**

---

## 📊 Dashboard Pages

| Page | Description |
|---|---|
| 📊 Executive Overview | 8 KPI cards + 7 interactive charts with full sidebar filters |
| 👥 Patient Analytics | Demographics, blood type, segmentation scatter, insurance breakdown |
| 🩺 Clinical Analytics | Condition heatmaps, medication pie, test results, LOS by condition |
| 🏥 Hospital Operations | Top hospitals bar, LOS histogram, admissions heatmap (Year × Month) |
| 💰 Financial Analytics | Revenue area chart, billing by condition/insurance/hospital, revenue category |
| 🤖 Predictive Analytics | Model comparison table, ROC curves, confusion matrix, feature importance, individual prediction form |
| 💡 Insights & Recommendations | 13 auto-generated insights + 6 strategic recommendations + KPI table download |

### Dashboard Filters (Sidebar)

- 📅 Admission Date Range
- ⚧ Gender
- 👥 Age Group
- 🩺 Medical Condition
- 🏨 Admission Type
- 🛡️ Insurance Provider
- 🏥 Hospital

All filters update every chart in real time.

---

## 📈 Healthcare KPIs

| # | KPI | Description |
|---|---|---|
| 1 | Total Patients | Count of all patient records |
| 2 | Total Admissions | Total admission events |
| 3 | Total Discharges | Count of patients with valid discharge dates |
| 4 | Active Patients | Patients with future discharge dates |
| 5 | Average Patient Age | Mean age of patient cohort |
| 6 | Avg Length of Stay | Mean days between admission and discharge |
| 7 | Total Healthcare Revenue | Sum of all billing amounts |
| 8 | Average Billing Amount | Mean billing per patient |
| 9 | Readmission Rate (%) | % patients with inconclusive test results (proxy) |
| 10 | Abnormal Outcome Rate | % patients with abnormal test results |
| 11 | Most Common Condition | Modal medical condition |
| 12 | Emergency Admission % | % emergency vs all admissions |
| 13 | High-Risk Patient % | % flagged as high-risk |
| 14 | Top Insurance Provider | Most common insurance |
| 15 | Peak Admission Month | Month with highest admissions |
| 16 | Avg Age | Average patient age |
| 17 | Busiest Hospital | Hospital with most patients |

---

## 🤖 Machine Learning — Readmission Risk Prediction

### Target Variable
`Readmission` — derived from `Test_Results == 'Inconclusive'` (proxy indicator)

### Features Used
Age, Billing Amount, Length of Stay, Gender, Medical Condition, Admission Type, Insurance Provider, Medication, Test Results, Blood Type, Age Group

### Models Trained
- Logistic Regression
- Decision Tree (max_depth=6)
- Random Forest (100 estimators)
- Gradient Boosting (100 estimators)

### Evaluation Metrics
- Accuracy, Precision, Recall, F1-Score
- ROC-AUC Score
- Confusion Matrix
- ROC Curve

### Model Selection
Best model selected by ROC-AUC score. Saved to `models/readmission_model.pkl`.

> ⚠️ **Disclaimer:** All models are for **educational and analytical purposes only**. They are NOT a medical diagnosis system and must NOT be used for clinical decision-making.

---

## 💡 Key Insights (Auto-Generated)

Insights are generated dynamically from actual data calculations. Examples:
- Most prevalent medical condition and its share of total patients
- Emergency admission percentage
- Readmission rate based on test result proxy
- High-risk patient percentage
- Revenue and billing statistics
- Age group with highest patient volume
- Peak admission month
- Busiest hospital by volume

---

## ⚠️ Limitations

1. **No real patient data** — dataset is synthetic/anonymized
2. **Readmission proxy** — uses Test_Results == 'Inconclusive' as a proxy; a real readmission field would improve accuracy
3. **No true clinical validation** — ML models are not validated for clinical use
4. **No real-time data** — dashboard works with static CSV data
5. **Single-hospital aggregation** — no true department/ward-level granularity in dataset

---

## 🔒 Ethical Considerations

- All patient data is **synthetic and anonymized** — no real individuals are identified
- ML predictions are for **analytical and educational purposes only**
- No clinical or medical claims are made
- Models should NOT be used to make healthcare decisions
- Data privacy and HIPAA compliance are critical in real-world deployments

---

## 🔭 Future Enhancements

- [ ] Real-time data ingestion via hospital APIs or HL7 FHIR
- [ ] NLP-based clinical notes analysis
- [ ] Deep learning models (LSTM for time-series forecasting)
- [ ] Hospital department-level granularity
- [ ] Patient outcome tracking (survival analysis)
- [ ] Role-based access control (admin, doctor, analyst)
- [ ] Cloud deployment (AWS / Azure / GCP)
- [ ] Automated PDF report generation

---

## 👩‍💻 Author

**Sheetal**  
Data Science & Healthcare Analytics Project  
*Healthcare Insight360 — AI-Powered Analytics & Patient Intelligence*

---

## 📄 License

This project is licensed under the MIT License.

---

> ⚠️ **Important:** This project uses a **synthetic healthcare dataset** for educational purposes. It does not contain real patient data and should NOT be used for clinical or medical decision-making.
