### **Project Overview**  
The **Predictive Maintenance System** leverages machine learning models to predict machine failures, enabling organizations to perform proactive maintenance and reduce equipment downtime. This project focuses on analyzing industrial sensor data, engineering relevant features, and applying supervised learning techniques to classify machine health.

---

### **Objective**  
To build a robust machine learning-based system that predicts machine failures based on historical sensor data, enhancing maintenance schedules and minimizing unexpected operational disruptions.

---

### **Dataset Details**  
- **Dataset**: AI4I 2020 Predictive Maintenance dataset with **10,000 instances**.  
- **Features**: Includes attributes such as:  
  - **Air Temperature (K)**  
  - **Process Temperature (K)**  
  - **Rotational Speed (rpm)**  
  - **Torque (Nm)**  
  - **Tool Wear (min)**  
  - Failure Modes: Tool Wear Failure (TWF), Heat Dissipation Failure (HDF), Power Failure (PWF), Overstrain Failure (OSF), Random Failures (RNF).  
- **Target Variable**: Binary label indicating machine failure (1: Failure, 0: No Failure).  

---

### **Steps and Methodology**  

#### **1. Data Exploration and Cleaning**  
- **Exploratory Data Analysis (EDA)**:  
  - Examined distributions of numerical features using histograms and KDE plots.  
  - Plotted a heatmap of feature correlations to identify dependencies and multicollinearity.  
- **Data Cleaning**:  
  - Checked for missing values and duplicates (none detected).  
  - Normalized column names for compatibility with machine learning frameworks.  

#### **2. Feature Engineering**  
- Analyzed the **relationship between failure modes and sensor readings** to identify key predictors.  
- Explored **statistical properties** of features, such as mean, standard deviation, and outliers, to ensure data integrity.  

#### **3. Data Preprocessing**  
- **Feature Scaling**: Used **StandardScaler** to normalize numerical features for better model performance.  
- **Train-Test Split**: Divided the dataset into 80% training and 20% testing subsets to evaluate model generalization.

#### **4. Model Development**  
Implemented and compared the following machine learning models:  
1. **XGBoost Classifier**:  
   - Achieved high accuracy through gradient boosting.  
   - Tuned hyperparameters, including `n_estimators`, for optimal results.  
2. **Random Forest Classifier**:  
   - Utilized an ensemble of decision trees to improve classification performance.  
   - Delivered a weighted F1-score of 0.98, indicating high reliability in failure prediction.  
3. **Bagging Classifiers**:  
   - Tested with **Decision Tree** and **Logistic Regression** base estimators.  
   - Demonstrated effective ensemble learning to reduce overfitting.  

#### **5. Evaluation Metrics**  
- **Confusion Matrix**: Analyzed True Positives (TP), False Positives (FP), True Negatives (TN), and False Negatives (FN).  
- **Classification Report**: Measured precision, recall, F1-score, and support.  
  - **Overall Accuracy**: 99% across models.  
  - **High Precision**: Ensured minimal false positives in predicting failures.  
  - **Balanced Recall**: Addressed imbalanced class distributions effectively.

#### **6. Visualization and Insights**  
- Plotted **pairwise feature relationships** using Seaborn’s pairplot to visualize class separability.  
- Used **heatmaps** to highlight correlations between sensor features and failure outcomes.  
- Generated **bar plots** to visualize distributions of machine types and failure counts.

#### **7. Model Deployment Preparation**  
- **Pipeline Design**: Created an end-to-end pipeline integrating data preprocessing, feature scaling, and model prediction.  
- **Model Persistence**: Saved trained models, scalers, and column mappings using Joblib for future deployment.

---

### **Key Results**  
- **Accuracy**: Achieved 99% on the test set for failure classification.  
- **Performance**: Models demonstrated strong F1-scores, ensuring reliable predictions across failure and non-failure classes.  
- **Insights**: Identified features like **rotational speed**, **torque**, and **tool wear** as critical predictors of machine health.

---

### **Tools and Technologies Used**  
- **Languages**: Python  
- **Libraries**: Pandas, NumPy, scikit-learn, XGBoost, Matplotlib, Seaborn  
- **Techniques**: Feature scaling, ensemble learning, and hyperparameter tuning  

---

### **Impact and Applications**  
The Predictive Maintenance System is designed to minimize unplanned equipment failures, reduce operational costs, and optimize maintenance schedules. It is scalable across industries, including manufacturing, energy, and transportation, to improve efficiency and reliability.
