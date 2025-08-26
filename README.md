# CSCI218 (SP125) - Foundations of AI (Group 32)
## **CDC Diabetes Health Indicators (BRFSS-2014) Classification Project**

**Group Members**
*   Ng Teng Boon (8963794)
*   Jeslyn Ho Ka Yan (8535383)
*   Lester Liam Chong Bin (7558752)
*   Micah Angeles Josephine Flores (8575289)
*   Chea Darayuth (8550864)
*   Bryce Nicolas Fernandez Sumcad (8561369)

**🎬 Check Out Our Presentation:** [https://youtu.be/E6VkSWyGdDM?si=oPbGZMQIzqdnAZbL](https://youtu.be/E6VkSWyGdDM?si=oPbGZMQIzqdnAZbL)

**⭐ Review our Analysis/Notebook:**

---

## Introduction
Diabetes is a global health concern affecting millions of people, hence early detection can help prevent severe complications. Through Machine Learning, we can improve prediction and accuracy based on current available health data. This project focuses analysing, training and evaluating different machine learning models to solve a binary classification problem. The objective is to accurately predict whether a person is at risk of "Pre-Diabetic/Diabetes" or "No Diabetes" using **behavioural risks** on data provided by the CDC Diabetes Health Indicators (BRFSS 2014) dataset available on [UCI Repository](https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators).

## Literature Review
Previous studies by Ren (2024) shows that the best performing model CAT Boost had a test precision of 55.6%, with an overall test accuracy of 86.6%. One **key challenge** faced in this project include imbalanced dataset, where the ratio of No Diabetes to Diabetes is significantly higher, resulting in the model being biased towards the majority class. In this study, SMOTE oversampling was applied to increase the number of diabetes samples.

## Our Implementation/Methodology
* **Data Processing:** Handling missing values, duplicates, scaling features
* **Exploratory Data Analysis:** Analysed various Risk Factors against Diabetes
* **Feature Engineering:** Developed new features influencing diabetes, such as BMI Category, High Risk Factor, Lifestyle Risk Factors
* **Feature Selection:** Chi-Squared Test, Correlation Matrix
* **Model Training:** Compared multiple models, including Deep Learning (MLP Classifier, XGB Classifier & RandomForest etc.)
* **Resampling Dataset:** Using [imblearn](https://imbalanced-learn.org/stable/) package, evaluated different oversampling and undersampling strategies to observe how it affect model performance.

### Results
XGBoost Classifier and MLP Classifier with undersampling with TomekLinks resulted in our best performing model, averaging 85% accuracy, 55% precision and recall of 23%. Before undersampling, recall was around 15%, hence a small increase could be observed with undersampling strategy. This could be due to TomekLinks removing difficult to classify data points, resulting in the model generalising better.


## References
> 1. Teboul, Alex. (2014). CDC Diabetes Health Indicators. The UCI Machine Learning Repository. [10.24432/C53919](https://doi.org/10.24432/C53919)<br/>
> 2. Ren, Xinyi. (2024). Predictions of diabetes through machine learning models based on the health indicators dataset. Applied and Computational Engineering. 32. 216-222. [10.54254/2755-2721/32/20230214](http://dx.doi.org/10.54254/2755-2721/32/20230214). 
