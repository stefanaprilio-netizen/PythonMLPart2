# ANTAM Gold Price MLOps Project

**Status**: 🚀 In Development (Phase 1 - Baseline Complete)  
**Last Updated**: March 15, 2026  
**Dataset Downloaded**: ✅ Yes (4,893 records)

## 📋 Project Overview

Sistem prediksi harga emas ANTAM dengan Machine Learning Operations (MLOps) pipeline yang komprehensif. Project ini menggabungkan:

- **Data Science**: Time series analysis dan forecasting
- **Machine Learning**: Multiple algorithms untuk comparison
- **MLOps**: Model registry, monitoring, dan automated pipeline

### Dataset

- **Source**: [ANTAM Historical Gold Price - Kaggle](https://www.kaggle.com/datasets/garethharrison/antam-historical-gold-price)
- **File**: `Antam_historical_gold_prices.csv` (206.75 KB)
- **Period**: 2010-01-04 hingga 2025-10-07
- **Currency**: IDR (Indonesian Rupiah)
- **Columns**: Time (ms), Gold Price, Date, dan derived features
- **License**: MIT

---

## 🏗️ Project Structure

```text
ANTAM_Gold_Price_MLOps/
├── ANTAM_Gold_Price_MLOps.ipynb     ← Main notebook
├── README.md                         ← Project documentation
├── data/
│   ├── Antam_historical_gold_prices.csv    (Raw data from Kaggle)
│   ├── data_processed.csv                  (Cleaned & engineered data)
│   ├── train_data.csv                      (80% training set)
│   ├── test_data.csv                       (20% test set)
│   └── eda_analysis.png                    (Visualizations)
└── models/
    ├── model_registry.json                 (Model metadata)
    └── training_log.json                   (Training metrics log)
```

---

## 🚀 Quick Start

### Prerequisites

```bash
# Python 3.8+
python --version

# Install dependencies
pip install pandas numpy matplotlib seaborn plotly scikit-learn tensorflow prophet statsmodels kaggle
```

### Setup Kaggle API

1. Go to <https://www.kaggle.com/settings/account>
2. Click "Create New API Token"
3. Download `kaggle.json`
4. Place in `~/.kaggle/kaggle.json` (Linux/Mac) atau `C:\Users\YourUsername\.kaggle\kaggle.json` (Windows)

### Download Dataset & Run Notebook

```bash
# Download dataset
kaggle datasets download -d garethharrison/antam-historical-gold-price

# Extract to ./data folder
# Then run the notebook in VS Code or Jupyter
jupyter notebook ANTAM_Gold_Price_MLOps.ipynb
```

---

## 📊 Project Progress

### Phase 1: Baseline ✅ (COMPLETED)

**Deliverables:**

- [x] **Data Loading & Exploration** ✅ COMPLETED
  - ✓ Load CSV dari Kaggle (4,893 records)
  - ✓ Basic statistics & missing values check
  - ✓ Temporal coverage: 15 tahun data historis
  
- [x] **Data Preprocessing** ✅ COMPLETED
  - ✓ Handle missing values
  - ✓ Parse timestamps (Unix milliseconds → datetime)
  - ✓ Extract time features (year, month, day, weekday, quarter)
  - ✓ Calculate technical indicators (MA-7, MA-30, MA-90)
  - ✓ Compute daily returns & volatility
  - ✓ Output: data_processed.csv
  
- [x] **Exploratory Data Analysis (EDA)** ✅ COMPLETED
  - ✓ Time series trend visualization
  - ✓ Moving averages analysis
  - ✓ Daily returns distribution
  - ✓ Volatility trend (30-day rolling)
  - ✓ Statistical summary
  - ✓ Output: eda_analysis.png
  
- [x] **Train-Test Split** ✅ COMPLETED
  - ✓ 80-20 time series split
  - ✓ train_data.csv: 3,914 records
  - ✓ test_data.csv: 979 records
  
- [x] **Baseline Model** ✅ COMPLETED
  - ✓ Naive Forecast (last value as prediction)
  - ✓ Baseline metrics evaluated:
    - RMSE
    - MAE
    - MAPE
  
- [x] **MLOps Framework** ✅ COMPLETED
  - ✓ Model Registry JSON (model_registry.json)
  - ✓ Training Log System (training_log.json)
  - ✓ Model Comparison Tool
  - ✓ Metrics tracking

**Execution Status:**

- ✅ All 7 notebook cells executed successfully
- ✅ Dataset downloaded: 4,893 records
- ✅ Data processing: Complete
- ✅ EDA visualizations: Generated (eda_analysis.png)
- ✅ Baseline model: Trained & evaluated
- ✅ MLOps registry: Active

**Key Statistics:**

- Total Records: 4,893 price points
- Date Range: 2010-01-04 to 2025-10-07
- Avg Daily Return: < 1%
- Price Range: IDR 200,000 - 1,500,000+ per gram
- Files Generated: 6 data files + 1 visualization

---

### Phase 2: Advanced Models 🔄 (TODO)

**Planned Models:**

- [ ] ARIMA/SARIMA (Statistical time series)
- [ ] Facebook Prophet (Additive model)
- [ ] XGBoost (Gradient boosting dengan lagged features)
- [ ] LSTM RNN (Deep learning)

**Tasks:**

- [ ] Hyperparameter tuning
- [ ] Cross-validation strategy
- [ ] Model comparison & selection
- [ ] Residual analysis

---

### Phase 3: Production & Deployment 📦 (TODO)

**Infrastructure:**

- [ ] Model versioning (DVC/MLflow)
- [ ] API development (FastAPI/Flask)
- [ ] Docker containerization
- [ ] CI/CD pipeline (GitHub Actions)
- [ ] Cloud deployment

**Services:**

- [ ] Real-time prediction API
- [ ] Batch prediction service
- [ ] Model registry dashboard

---

### Phase 4: Monitoring & Maintenance 📈 (TODO)

**Monitoring:**

- [ ] Performance dashboard
- [ ] Data drift detection
- [ ] Model performance degradation alert
- [ ] Retraining trigger logic
- [ ] A/B testing framework

**Maintenance:**

- [ ] Automated retraining schedule
- [ ] Model evaluation pipeline
- [ ] Logging & debugging
- [ ] Production troubleshooting

---

## 📈 Notebook Contents

| Section | Status | Description |
| --- | --- | --- |
| 1. Setup & Libraries | ✅ | Import dependencies |
| 2. Data Loading | ✅ | Load dari Kaggle |
| 3. Preprocessing | ✅ | Cleaning & feature engineering |
| 4. EDA & Visualization | ✅ | Exploratory analysis |
| 5. Model Development | 🔄 | Training & evaluation |
| 6. MLOps Pipeline | ✅ | Framework & registry |
| 7. Roadmap | 📋 | Future phases |
| 8. Documentation | ✅ | Notes & references |

---

## 🔧 Technical Stack

| Component | Tools |
| --- | --- |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn, Plotly |
| **ML/Stats** | scikit-learn, Prophet, statsmodels |
| **Deep Learning** | TensorFlow/Keras |
| **Gradient Boosting** | XGBoost |
| **MLOps** | Custom Registry, JSON logging |
| **API** | FastAPI (planned) |
| **Container** | Docker (planned) |
| **Version Control** | Git/GitHub |

---

## 📚 Key Metrics Explained

### RMSE (Root Mean Squared Error)

- Mengukur rata-rata magnitude error
- Lebih sensitif terhadap outliers
- Unit: sama dengan target variable (IDR)

### MAE (Mean Absolute Error)

- Mengukur rata-rata absolute error
- Lebih robust terhadap outliers
- Unit: sama dengan target variable (IDR)

### MAPE (Mean Absolute Percentage Error)

- Mengukur error dalam persentase
- Bagus untuk comparison across different scales
- Unit: %

---

## 🎓 Learning Outcomes

Dari project ini, Anda akan belajar:

1. ✅ Time series data analysis
2. ✅ Feature engineering untuk time series
3. ✅ MLOps pipeline implementation
4. ✅ Model evaluation & comparison
5. 🔄 Hyperparameter tuning (Phase 2)
6. 🔄 Model deployment (Phase 3)
7. 🔄 Production monitoring (Phase 4)

---

## 📝 Usage Examples

### Download & Prepare Data

```python
# Uncomment di notebook untuk download
!kaggle datasets download -d garethharrison/antam-historical-gold-price

# Data akan tersimpan di ./data folder
```

### Load Processed Data

```python
import pandas as pd
df = pd.read_csv('./data/data_processed.csv')
print(df.head())
print(df.describe())
```

### Check Model Metrics

```python
# Model comparison akan otomatis ditampilkan
# Metrics tersimpan di ./models/training_log.json
```

---

## 🤝 Contributing

Untuk berkontribusi:

1. Buat branch baru untuk fitur/perbaikan
2. Update dokumentasi
3. Test sebelum push
4. Create pull request with description

---

## 📞 Support & Questions

- **Dataset Issues**: Check [Kaggle Dataset Page](https://www.kaggle.com/datasets/garethharrison/antam-historical-gold-price)
- **Kaggle API Help**: <https://github.com/Kaggle/kaggle-api>
- **Time Series Forecasting**: [statsmodels docs](https://www.statsmodels.org/)
- **Prophet**: [Facebook Prophet Docs](https://facebook.github.io/prophet/)

---

## 📄 License

- **Dataset**: MIT License (per Kaggle)
- **Project Code**: MIT License

---

## 🗺️ Roadmap Timeline

```text
Phase 1: ✅ Complete (Mar 2026)
  ├─ Data loading & preprocessing
  ├─ EDA & visualization
  └─ Baseline model & MLOps framework

Phase 2: 🔄 Expected (Apr 2026)
  ├─ Advanced models
  ├─ Hyperparameter tuning
  └─ Model comparison

Phase 3: 📋 Planned (May 2026)
  ├─ API development
  ├─ Containerization
  └─ CI/CD pipeline

Phase 4: 📋 Planned (Jun 2026)
  ├─ Monitoring dashboard
  ├─ Data drift detection
  └─ Automated retraining
```

---

**Last Commit**: March 15, 2026  
**Last Execution**: March 15, 2026 - All 7 cells executed successfully ✅  
**Next Review**: When Phase 2 completes  
**Maintainer**: MLOps Team
