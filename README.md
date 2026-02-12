# 🏥 Kerala Healthcare Resource Optimization  


---

## 📌 Project Overview

This project focuses on optimizing healthcare resource allocation across Kerala districts using Machine Learning and Linear Programming techniques.

The objective is to:

- Predict healthcare infrastructure stress  
- Identify high-risk districts  
- Simulate surge demand scenarios  
- Minimize unmet healthcare demand  
- Provide data-driven policy insights  

This project integrates predictive modeling with optimization to support strategic healthcare planning.

---

## 🎯 Problem Statement

How can we optimize the allocation of beds, ICU units, ventilators, and medical staff across districts to reduce unmet demand during high-stress scenarios such as pandemics or natural disasters?

---

## 📊 Data Source

Data was collected from:

**Government of Kerala – Healthcare Infrastructure Reports (2023–24)**

Extracted district-level data includes:

- Total hospital beds  
- ICU beds  
- Ventilators  
- Ambulances  
- Doctors  
- Nurses  
- Inpatient (IP) demand  
- Outpatient (OP) demand  

Raw PDF reports were converted into structured CSV datasets and merged into a unified dataset.

---

## 📁 Project Structure

## 📁 Project Structure
```text
Healthcare Resource Optimization/
│
├── data/
│   ├── raw/                  # Extracted district-level CSV files  
│   └── processed/            # Final merged dataset  
│
├── models/                   # Trained ML model files (.pkl)  
│   ├── ridge_model.pkl  
│   ├── linear_model.pkl  
│   ├── gradient_boosting_model.pkl  
│   ├── extra_trees_model.pkl  
│   └── random_forest_model.pkl  
│
├── notebooks/  
│   ├── 01_data_collection.ipynb  
│   ├── 02_feature_engineering.ipynb  
│   ├── 03_linear_programming_optimization.ipynb  
│   ├── 04_model_building.ipynb  
│   └── 05_visualization.ipynb  
│
├── results/                  # Plots, tables, performance comparisons  
│
└── README.md
```


---

## 🧹 Data Preprocessing

- Handled missing values  
- Standardized district names  
- Verified data consistency  
- Merged multiple datasets  
- Created structured processed dataset  

Final dataset:

`kerala_healthcare_infrastructure_2023_24.csv`

---

## ⚙️ Feature Engineering

Healthcare Stress Indicators were created:

- **Bed Stress Index** = IP Demand / Total Beds  
- **ICU Stress Index** = IP Demand / ICU Beds  
- **Ventilator Stress Index** = IP Demand / Ventilators  
- **Doctor Load** = IP Demand / Doctors  
- **Nurse Load** = IP Demand / Nurses  
- **Ambulance Risk Index** = IP Demand / Ambulances  
- **Demand Risk Index** (Composite normalized metric)  

These features quantify district-level healthcare pressure.

---

## 📈 Exploratory Data Analysis

- District risk ranking tables  
- Healthcare stress heatmaps  
- Demand comparison charts  
- Resource load visualizations  

**Key Insight:**  
Certain districts consistently exhibit higher infrastructure stress.

---

## 🤖 Machine Learning Models

The following models were trained and evaluated:

1. Linear Regression  
2. Ridge Regression  
3. Gradient Boosting  
4. Extra Trees  
5. Random Forest  

### 📊 Evaluation Metrics

- MAE (Mean Absolute Error)  
- RMSE (Root Mean Square Error)  
- R² Score  

---

## 🏆 Model Selection

**Selected Model: Ridge Regression**

### Why Ridge?

- Lowest RMSE  
- Highest R² Score  
- More stable generalization  
- Handles multicollinearity effectively  
- Reduced overfitting compared to tree-based models  

Ridge Regression demonstrated the best predictive performance for structured district-level healthcare data.

---

## 🚨 Stress Testing Simulation

Demand surge multipliers simulated from:1.0x → 2.0x


Measured:

- Unmet bed demand  
- ICU capacity failure  
- Ventilator shortages  
- District failure stages  

### Key Finding:

System failure increases significantly beyond **1.6x surge multiplier**.

---

## 📐 Linear Programming Optimization

**Objective:**  
Minimize unmet healthcare demand under resource constraints.

Constraints considered:

- Bed capacity limits  
- ICU capacity limits  
- Ventilator limits  
- District allocation boundaries  

**Output:**  
Optimized resource redistribution strategy under surge conditions.

---

## 🔎 Key Insights

- High-risk districts identified through Demand Risk Index  
- ICU and ventilator shortages drive early system failure  
- Ridge Regression provides most reliable predictions  
- Surge scenarios highlight infrastructure vulnerabilities  
- Optimization reduces district-level imbalance  

---

## 🏛 Policy & Business Impact

This framework can support:

- Emergency preparedness planning  
- District-level healthcare budgeting  
- Infrastructure gap analysis  
- Pandemic surge planning  
- Data-driven government decision-making  

---

## 🛠 Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  
- PuLP (Linear Programming)  
- Google Colab  

---

## 🚀 Future Improvements

- Time-series demand forecasting  
- Real-time dashboard integration  
- Deployment using Streamlit or FastAPI  
- Integration with live healthcare APIs  

---

## 👩‍💻 Author

**Tabassum Unnisa**  








