# Diabetes EDA and Classification

This project focuses on analyzing and classifying diabetes using the Pima Indians Diabetes dataset. It includes comprehensive Exploratory Data Analysis (EDA), feature treatment, and machine learning model evaluation to predict the presence of diabetes.

## 🧾 Objective

- Clean and prepare healthcare data for analysis
- Discover patterns using EDA and statistical methods
- Build and evaluate classification models
- Reduce false negatives using threshold tuning

## 📊 Dataset

- **Source:** Pima Indians Diabetes Dataset
- **Rows:** 768
- **Features:** 8 medical features + Outcome (0: No Diabetes, 1: Diabetes)

## ⚙️ Data Cleaning

- Zero values in features like Glucose, BloodPressure, SkinThickness, etc., were treated as missing.
- Replaced zero values with:
  - **Median** for most features
  - **Mean** for Insulin due to skewness
- Data was normalized using `StandardScaler`.

## 📈 Exploratory Data Analysis (EDA)

- Point biserial correlation was used to evaluate feature-target relationships.
- Top influential features: Glucose, BMI, Insulin
- Visualizations:
  - Histograms
  - Box plots (outlier detection)
  - Pair plots (class separation)
  - Heatmaps (feature correlation)

## 🤖 Model Training & Evaluation

| Model          | Accuracy | Notes                                 |
|----------------|----------|---------------------------------------|
| K-Nearest Neighbors (k=35) | 83%      | Best performing baseline model       |
| Support Vector Machine     | 77%      | Linear kernel                        |
| Random Forest              | 82%      | Balanced precision and recall        |

### ✅ Threshold Optimization

- Changed default classification threshold from 0.5 to ~0.35 to minimize **false negatives**, which is crucial in medical diagnosis.

## 🗃️ Output

- Final prediction file: `diabetes classification report.csv`

## 🛠️ Technologies Used

- Python
- Pandas, NumPy
- Seaborn, Matplotlib, Plotly
- Scikit-learn
- SciPy

