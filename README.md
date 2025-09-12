🩺 Diabetes Prediction with Machine Learning

This project develops a machine learning system to predict diabetes based on diagnostic health measurements from the Pima Indians Diabetes Dataset. The goal is to provide an accurate and practical tool for early diabetes detection, supporting better patient management and prevention of complications.

📊 Dataset

Source: National Institute of Diabetes and Digestive and Kidney Diseases

Patients: Female, ≥21 years old, Pima Indian heritage

Size: 768 instances, 8 features + 1 outcome

Features: Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, Age

Target: Outcome → 1 (Diabetic) or 0 (Non-Diabetic)

Preprocessing: Missing values (zeroes) imputed, features scaled, SMOTE applied to balance classes

🔎 Exploratory Data Analysis (EDA)

Glucose: Strongest predictor, positively correlated with diabetes outcome

BMI: Significant positive relationship with diabetes outcome

Pregnancies & Age: Moderate correlation with diabetes risk

Correlation Heatmap & Boxplots confirmed glucose and BMI as key risk factors

🤖 Models Compared

Four machine learning algorithms were trained and tuned with GridSearchCV (5-fold CV):

Logistic Regression → Accuracy: 75%

Support Vector Classifier (SVC) → Accuracy: 81%, strong overall performance

Random Forest → Accuracy: 79%, highest ROC-AUC (0.86) and recall (best at detecting diabetics)

Gradient Boosting (tested but not best performer)

✅ Results & Conclusion

Random Forest selected as the best model due to its balanced performance, strong ROC-AUC, and reliability in identifying both diabetic and non-diabetic patients.

Logistic Regression and SVC also performed well, but RF was the most robust for healthcare deployment.

🚀 Deployment

The final model can be deployed as a prediction engine using tools like Gradio or FastAPI, allowing users to input patient data and instantly receive a diabetes risk prediction.
