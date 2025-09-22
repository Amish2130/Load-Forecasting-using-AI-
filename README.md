#  Load Forecasting Using Artificial Intelligence

This project predicts future **energy demand** using machine learning models such as **XGBoost** **LightGBM** **AdaBoost**.  
It was developed as a **Final Year Project** to help utilities and energy planners anticipate demand for the upcoming months, improve resource allocation, and reduce energy shortages.

---

##  Project Overview
Accurate load forecasting is critical for power generation planning.  
Our solution uses **10+ years of historical demand data**, performs **feature engineering** (rolling averages, seasonal & holiday flags), and applies multiple machine learning models to predict demand for the next 6–12 months.

---

## My Role & Contribution
This was a **group project**, but here’s what I specifically worked on:
-  **Data Cleaning & Preprocessing:** Handled missing values, outliers, and resampled data into daily/quarterly resolution.  
-  **Feature Engineering:** Created lag features, moving averages, holiday indicators, and temperature-based variables.  
-  **Model Implementation:** Built and tuned **XGBoost** and **ARIMA** models, compared results with other algorithms.  
-  **Visualization:** Generated quarterly trend graphs and interactive plots for better insights.  
-  **Documentation:** Wrote this README and contributed to final report + presentation slides.

---

## Project Structure
project/
├── data/ # Processed datasets (cleaned data only)
├── notebooks/ # Jupyter notebooks for EDA, feature engineering, and modeling
├── scripts/ # Helper scripts for preprocessing & training
├── images/ # Visualizations & screenshots
└── README.md

---

## ⚙️ How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/load-forecasting-ai.git
   cd load-forecasting-ai
pip install -r requirements.txt

jupyter notebook notebooks/forecast.ipynb
## 🧪 Experimental Results

The performance of the models is summarized below:

| Model                  | MAE       | RMSE      | R² Score |
|-----------------------|-----------|-----------|----------|
| Linear Regression     | 1371.743 | 1648.475 | 0.9268 |
| Lasso Regression      | 1371.309 | 1650.458 | 0.9267 |
| Ridge Regression      | 1371.659 | 1648.984 | 0.9268 |
| Elastic Net Regression| 1374.783 | 1693.873 | 0.9228 |
| K-Nearest Neighbors   | 1994.994 | 2790.478 | 0.7904 |
| Random Forest         | **567.838** | **807.768** | **0.9824** |
| AdaBoost Regressor    | 1406.238 | 1785.744 | 0.9142 |
| Gradient Boosting     | **581.288** | **737.606** | **0.9854** |
| XGBoost Regressor     | 1371.734 | 1648.953 | 0.9268 |
| LightGBM Regressor    |  **555.756** | **710.347** |  **0.9864** |
| CatBoost Regressor    | 598.650 | 734.249 | 0.9855 |

### 📊 Key Insights
- **LightGBM** was the best performer across all metrics, achieving the lowest error and highest R² score.  
- **Gradient Boosting** and **CatBoost** were close competitors, showing strong generalization.  
- Simpler models like Linear/Lasso/Ridge showed good baseline performance but higher error compared to tree-based models.  
- **KNN performed poorly**, likely due to high dimensionality and lack of feature scaling optimization.
