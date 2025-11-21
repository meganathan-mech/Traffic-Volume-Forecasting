# 🚦 Traffic Volume Forecasting using Deep Learning

### 📌 Project Overview
This project focuses on predicting hourly traffic volume using a Bidirectional LSTM model integrated with a Bahdanau Attention mechanism. The model helps improve smart city traffic management by forecasting peak and off-peak road usage.

---

### 📊 Dataset
- **Dataset:** Metro Interstate Traffic Volume
- **Source:** UCI ML Repository / Kaggle
- **Features Used:**
  - Traffic Volume (Target)
  - Temperature (`temp`)
  - Rain (`rain_1h`)
  - Snow (`snow_1h`)
  - Cloud Coverage (`clouds_all`)

---

### 🧹 Data Preprocessing
- Datetime conversion & sorting
- Feature selection
- Handling missing values using forward fill
- Normalization using MinMaxScaler
- Time-series sliding window (24 previous hours → next hour)

---

### 🧠 Model Architecture
| Component | Details |
|----------|---------|
| Input | 24×5 feature window |
| Bi-LSTM | 128 units each direction |
| Attention | Bahdanau mechanism |
| Dense Layers | 64 → 1 |
| Loss | MSE |
| Optimizer | Adam |

The attention layer allows the network to focus on the most relevant time steps for prediction.

---

### 📈 Performance Metrics
| Metric | Value |
|--------|------|
| RMSE | **401.99** |
| MAE | **273.83** |
| MAPE | **13.77%** |

The model successfully captures daily traffic patterns and peak hours.

---

### 🗂 Output Files Included
📁 `/Final_Submission/`
| File | Description |
|------|-------------|
| `final_model.h5` / `final_model.keras` | Trained deep learning model |
| `scaler.save` | Normalization model used during training |
| `next_24hr_predictions.csv` | 24-hour forecast results |
| `Final_Report.pdf` (optional) | Complete project documentation |

---

### 🎯 Conclusion
✔ Strong performance on real traffic data  
✔ Fully automated forecasting pipeline  
✔ Ready for deployment and future upgrades  

---

### 🔮 Future Work
- Include additional real-time traffic indicators
- Implement Transformers to enhance long-term prediction
- Deploy web dashboard for live monitoring

---

### ⭐ Acknowledgement
This project is built for academic and research purposes.  
Contributions and improvements are welcome!

---

### 📌 License
Open for educational use.
