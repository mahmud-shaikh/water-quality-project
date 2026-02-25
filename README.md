💧 Water Quality Classification Using Machine Learning

📘 Project Overview

This project focuses on predicting whether a water sample is suitable for drinking or not using environmental and laboratory-based water quality parameters. The goal is to assist environmental monitoring authorities in identifying unsafe water sources and enabling data-driven decision-making for public health protection.

🎯 Objective

To build a supervised binary classification model that classifies water samples into:

1 → Good Water Quality (Suitable for drinking after disinfection)

0 → Not Suitable for Drinking

The model leverages chemical, physical, and environmental indicators to determine water safety status.

🧩 Dataset Information

Source: NWMP_August2025_MPCB_0.csv
Initial Dataset Size: 222 rows × 54 columns

🔄 Target Variable Transformation

Initially, the target variable “Use Based Class” contained multiple categories:

A

B

C

E

No Information

However, the dataset showed severe class imbalance:

Class A → 141 samples

Class B → 5 samples

Class C → 6 samples

Class E → Very few samples

Such extreme imbalance makes multi-class classification unstable and prone to biased predictions.

Additionally, “No Information” is not a valid water quality category and was removed.

From a practical and environmental perspective:

Class A represents water suitable for drinking (after disinfection).

Classes B, C, and E represent water not suitable for direct drinking.

Therefore, the problem was converted into a binary classification task:

1 (Good Water Quality) → Class A

0 (Not Suitable for Drinking) → Classes B, C, E

✅ Why Binary Transformation?

Improves model stability

Reduces classification complexity

Handles class imbalance more effectively

Aligns with real-world environmental decision-making

🧹 Final Cleaned Dataset

After cleaning and preprocessing:

Final Dataset Size: 171 rows × 42 columns

No missing values

No duplicate records

All categorical variables encoded into numerical form

Irrelevant and inconsistent features removed

The dataset is fully structured and ready for supervised machine learning.

⚙️ Data Preprocessing Steps

Removed “No Information” class

Converted multi-class target into binary classification

Handled categorical encoding

Verified data quality (missing values & duplicates)

Performed feature selection and cleaning

Split dataset into training and testing sets

🔍 Exploratory Data Analysis (EDA)

Analyzed class distribution after binary transformation

Examined correlation between water quality parameters

Identified influential features affecting drinking suitability

Used heatmaps and distribution plots for pattern analysis

Key Insight:

Certain chemical parameters showed stronger relationships with drinking suitability, helping improve model prediction performance.

🤖 Model Building
Algorithms Implemented

Logistic Regression

Random Forest Classifier

Hyperparameter Optimization

Used GridSearchCV to tune model parameters and improve generalization performance.

Evaluation Metrics

Accuracy

Precision

Recall

F1-Score

ROC-AUC

🏆 Final Model Selection

The Tuned Logistic Regression model was selected as the final model because:

It provided stable and balanced performance.

It improved detection of unsafe water samples.

It offers strong interpretability through feature coefficients.

It aligns well with environmental monitoring requirements.

💡 Key Results

Achieved strong classification accuracy.

Reduced instability caused by extreme multi-class imbalance.

Improved practical interpretability of predictions.

Developed a reliable system for drinking water classification.

🌍 Environmental Impact

Enables early detection of unsafe drinking water.

Supports regulatory water quality monitoring programs.

Reduces public health risks.

Promotes evidence-based environmental management.

🛠️ Tools & Libraries

Python

Pandas

NumPy

Scikit-learn

Matplotlib

Seaborn

Joblib

🚀 How to Run the Project
git clone <your-repository-link>
cd water-quality-project
pip install -r requirements.txt
jupyter notebook

Open:

notebooks/01_EDA.ipynb

notebooks/02_Modeling.ipynb

(Optional – Run Streamlit App)

streamlit run app.py
📈 Future Improvements

Apply SMOTE or advanced resampling techniques to handle imbalance.

Experiment with ensemble stacking models.

Deploy as a real-time water quality monitoring application.

Integrate with IoT-based environmental sensors.

👩‍💻 Author

Mahmud Shaikh
Machine Learning Project – Water Quality Classification
