# Weather Prediction using Machine Learning

## 📌 Overview
This project predicts whether it will rain based on historical weather data (Temperature, Humidity, Wind Speed, Cloud Cover, Pressure). It compares three classification algorithms to determine which best handles the weather patterns and class imbalance (majority "no rain" vs minority "rain").

## 🛠️ Tech Stack
- **Models:** Logistic Regression, Decision Tree, Random Forest
- **Libraries:** Scikit-learn, Pandas, Seaborn, Matplotlib
- **Dataset:** Weather Forecast Dataset (2,500 records)
- **Environment:** Google Colab / Local Jupyter

## 📊 Dataset Details
- **Features:** Temperature, Humidity, Wind_Speed, Cloud_Cover, Pressure
- **Target:** Rain (Binary: Rain / No Rain)
- **Split:** 80% Training (2,000 records) / 20% Testing (500 records)
- **Class Distribution:** Imbalanced (Majority "No Rain", Minority "Rain" at ~12.6%)

## 🚀 Methodology
1. **Data Cleaning:** Handled missing values and performed Label Encoding on the target variable.
2. **Feature Scaling:** Standardized numerical features to improve Logistic Regression performance.
3. **Model Training:** Trained Logistic Regression, Decision Tree, and Random Forest models using a stratified train-test split to maintain class balance.

## 📈 Results
| Model | Accuracy | Macro F1-Score | Observation |
| :--- | :--- | :--- | :--- |
| Logistic Regression | 92.60% | 0.83 | Struggles with complex non-linear patterns; lower recall on the minority "Rain" class. |
| Decision Tree | 99.80% | 1.00 | Excellent performance, but prone to overfitting on training data. |
| **Random Forest** | **100.00%** | **1.00** | **Best performer.** Achieved perfect precision and recall on this specific dataset. |

*(Note: The 100% accuracy indicates the dataset features are highly separable, and Random Forest easily captures these patterns.)*

## 💡 Key Takeaways
- **Ensemble Power:** Random Forest outperformed a single Decision Tree (99.8%) by combining multiple trees to reduce variance.
- **Linear Limitations:** Logistic Regression (92.6%) proved that simple linear decision boundaries are not sufficient for this specific weather classification task.
- **Feature Importance:** Tree-based models easily identified the critical thresholds (like specific humidity and pressure levels) that lead to rain.

## 🔗 How to Run
1. Open the `.ipynb` file in Google Colab.
2. Upload the `weather_forecast_data.csv` dataset to the Colab session.
3. Run all cells to view the accuracy comparison and the Confusion Matrix.
