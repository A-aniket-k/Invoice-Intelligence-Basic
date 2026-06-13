# 🤖 Vendor Invoice Intelligence Portal (Basic - Manual Mode)

A streamlined, lightweight Machine Learning and Data Analytics application built to evaluate logistics invoice risks and estimate freight baselines. This repository focuses strictly on localized predictive modeling via manual user inputs, providing a clean, fast, and stable operational layout.

---
## 📌 Core Overview & Problem Statement
Manual processing and validation of third-party logistics (3PL) invoices introduces administrative friction, financial leakages, and exposure to overcharging. 

**The Solution:** This basic configuration provides an interactive, standalone decision-support utility. By manually keying in specific transactional metrics, procurement and finance teams can immediately benchmark shipping expenses and audit compliance risks using trained local machine learning models without relying on heavy file parsing engines.

---

## 🛠️ Tech Stack & Architecture
* **Frontend Web App:** Streamlit (Clean, input-driven responsive utility forms)
* **Programming & Core Logic:** Python, Pandas, NumPy, Scikit-Learn
* **Model Deserialization:** Joblib
* **Deployment & Version Control:** Git, GitHub, Streamlit Community Cloud

---

## 💡 Key Modules & Features

### 🚛 Freight Cost Estimation Form
* **Dynamic Regression:** Accepts real-time values for cargo **Quantity** and raw **Invoice Dollars**.
* **Instant Baselines:** Leverages localized regression parameters to yield an instant target freight spot-rate estimation, ensuring shipping expenses scale predictably against historic vendor performance.

### 🔍 Risk & Manual Approval Flagging
* **Multi-Feature Assessment:** Evaluates compound variables simultaneously: *Invoice Quantity, Invoice Dollars, Freight Cost, Total Item Quantity,* and *Total Item Dollars*.
* **Anomalous Detection:** Instantly flags hidden overcharges or transaction discrepancies, clearly warning operators with a `⚠️ Invoice requires MANUAL APPROVAL` badge or confirming safety with a `✅ Safe for Auto-Approval` status.

---

## ⚙️ Local Setup & Installation

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/A-aniket-k/Invoice-Intelligence-Basic.git](https://github.com/A-aniket-k/Invoice-Intelligence-Basic.git)
   cd Invoice-Intelligence-Basic
2. **Install the Requirements:**
   ```bash
   pip install -r requirements.txt
3. **Boot Up the Local Dashboard:**
   ```bash
   streamlit run app.py      
## 📁 Project Structure

```text
Invoice-Intelligence-Basic/
│
├── .gitignore                          # Excludes temporary caches and environment files
├── README.md                           # Project documentation
├── app.py                              # Core Streamlit interactive dashboard script
├── requirements.txt                    # Minimal python package dependencies
│
├── Freight_Cost_Prediction/            # Training tracking distribution expense baselines
│   ├── data_preprocessing.py
│   ├── train.py
│   └── model_evaluation.py
│
├── invoice_flagging/                   # Training anomaly validation track
│   ├── data_preprocessing.py
│   ├── train.py
│   └── modeling_evaluation.py
│
└── inference/                          # Production runtime scoring layers
    ├── predict_freight.py              # Manual input freight cost estimator
    └── predict_invoice_flag.py         # Manual input compliance validation risk flag
