# 💤 Sleep Health & Lifestyle Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Pandas%20%7C%20Seaborn%20%7C%20ScikitLearn-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview
This project performs a comprehensive **Exploratory Data Analysis (EDA)** and **Statistical Inference** on the *Sleep Health and Lifestyle Dataset*. The goal is to identify lifestyle factors—such as occupation, BMI, and physical activity—that significantly impact sleep quality and the likelihood of sleep disorders.

Beyond standard visualization, this analysis incorporates **Feature Engineering** (parsing blood pressure data) and **Machine Learning** (Random Forest Feature Importance) to uncover non-linear relationships.

## 📂 Dataset
* **Source:** [Kaggle - Sleep Health and Lifestyle Dataset](https://www.kaggle.com/datasets/minahilfatima12328/lifestyle-and-sleep-patterns)
* **Rows:** ~400 entries
* **Features:** Gender, Age, Occupation, Sleep Duration, Quality of Sleep, Physical Activity Level, Stress Level, BMI Category, Blood Pressure, Heart Rate, Daily Steps, Sleep Disorder.

## 🛠️ Key Techniques Used

### 1. Data Cleaning & Preprocessing
* **Null Handling:** Imputed missing values in `Sleep Disorder` (assuming "None" for nulls).
* **Categorical Standardization:** Unified inconsistent labels (e.g., merging "Normal" and "Normal Weight").

### 2. Feature Engineering ⚙️
* **Blood Pressure Splitting:** Transformed the string column `Blood Pressure` (e.g., "126/83") into two numerical features: `Systolic_BP` and `Diastolic_BP`.
* **Pulse Pressure:** Calculated the difference between Systolic and Diastolic BP as a cardiovascular health indicator.

### 3. Statistical Analysis 📊
* **T-Test (Hypothesis Testing):** Validated the statistical significance of Stress Levels on Sleep Quality ($p < 0.05$).
* **Correlation Matrices:** Analyzed linear relationships between physiological markers.

### 4. Machine Learning & Inference 🤖
* **Random Forest Classifier:** Implemented to determine **Feature Importance**.
* **Result:** Identified that BMI Category and Systolic Blood Pressure are among the strongest predictors of Sleep Disorders, outweighing simple factors like Age.

## 📊 Key Insights
1.  **Occupation Matters:** Software Engineers and Sales Representatives reported lower sleep quality compared to Doctors and Nurses.
2.  **The Stress Factor:** There is a statistically significant difference in sleep quality between high-stress and low-stress groups.
3.  **Physical Activity:** A clear positive correlation exists between daily steps and sleep quality; however, this relationship plateaus at very high activity levels.

## 🚀 How to Run
1.  Clone the repository:
    ```bash
    git clone [https://github.com/yourusername/sleep-health-eda.git](https://github.com/yourusername/sleep-health-eda.git)
    ```
2.  Install dependencies:
    ```bash
    pip install pandas seaborn matplotlib scikit-learn plotly
    ```
3.  Run the Jupyter Notebook:
    ```bash
    jupyter notebook "Sleep_Analysis.ipynb"
    ```

## 📜 License
This project is open-source and available under the MIT License.
