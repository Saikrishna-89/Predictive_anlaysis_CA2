1.	Introduction

Education plays a vital role in shaping an individual’s future, and academic performance is influenced by various factors such as study habits, lifestyle choices, mental health, and family background. With the growing availability of data, machine learning techniques can be used to analyze these factors and predict student performance effectively.
This project focuses on performing predictive analysis on a student performance dataset to understand how different attributes such as study hours, sleep patterns, social media usage, attendance, and parental education impact exam results. The objective is to apply Exploratory Data Analysis (EDA) and build multiple machine learning classification models to predict student performance categories accurately.

2.	Source of dataset
The dataset used in this project is sourced from Kaggle, a well-known open platform for data science and machine learning resources. The dataset is titled “Student Habits vs Academic Performance” and is publicly available at:

🔗 https://www.kaggle.com/datasets/jayaantanaath/student-habits-vs-academic-performance

3.	The dataset used in this project was obtained from Kaggle, a popular online platform that provides open-source datasets for data science and machine learning projects. The dataset contains information related to student habits, lifestyle factors, and academic performance, including attributes such as study hours, sleep duration, attendance, parental education, and exam scores.
4.	The dataset was chosen because it is suitable for performing exploratory data analysis and predictive modeling, and it contains both numerical and categorical variables, making it ideal for applying multiple machine learning algorithms.

3.EDA process

Exploratory Data Analysis (EDA) is an essential step in understanding the structure, quality, and characteristics of the dataset before applying machine learning models. In this project, EDA was performed to gain insights into the data, identify patterns, and detect potential issues such as missing values and data imbalance.

3.1 Dataset Understanding
The first step in EDA involved examining the structure of the dataset. The number of rows and columns were checked to understand the size of the dataset. Data types of each column were analysed to differentiate between numerical and categorical variables. This helped in deciding appropriate preprocessing and visualization techniques.

3.2 Handling Missing Values
The dataset was checked for missing (null) values. Certain columns contained missing entries, which were handled using appropriate techniques:
•	Numerical columns were filled using statistical measures such as mean or median.
•	Categorical columns were filled using the mode (most frequent value).
Handling missing values ensured that the dataset was complete and suitable for further analysis and modelling.

3.3 Univariate Analysis
Univariate analysis was performed to understand the distribution of individual variables:
•	Histograms were used for numerical features such as study hours, sleep hours, and exam scores to observe their distribution patterns.
•	Count plots were used for categorical variables such as gender, diet quality, internet quality, and part-time job status to understand category frequencies.
This analysis helped identify skewness, concentration of values, and dominant categories in the dataset.
3.4 Outlier Detection and Treatment
Boxplots were used to identify outliers in numerical features like exam scores, study hours, and sleep hours. Outliers were detected using the Interquartile Range (IQR) method. Values lying below Q1 − 1.5 × IQR and above Q3 + 1.5 × IQR were considered outliers.
These outliers were removed to prevent them from negatively affecting the performance of machine learning models.

3.5 Bivariate Analysis
Bivariate analysis was conducted to study relationships between pairs of variables:
•	Boxplots were used to compare exam scores across categorical variables such as gender and part-time job status.
•	Pair plots were used to visualize relationships among multiple numerical features simultaneously.
•	These visualizations helped identify how different factors influence student performance.

3.6 Correlation Analysis
A correlation matrix was computed to examine the strength and direction of relationships between numerical variables. A heatmap was created to visually represent the correlation values. This analysis helped in identifying features that have a strong positive or negative relationship with exam scores.

3.7 Insights from EDA
The EDA process revealed several important insights:
•	Study hours and attendance showed a positive relationship with exam performance.
•	Adequate sleep and good mental health contributed to better scores.
•	Lifestyle factors such as excessive social media usage had a negative impact on performance.
•	Parental education and extracurricular participation also influenced student outcomes.

Overall, EDA played a significant role in understanding the dataset and guided effective feature selection and preprocessing for machine learning models.


4.Analysis on dataset
After completing the Exploratory Data Analysis (EDA), the dataset was further processed and analyzed using machine learning techniques to predict student performance. This stage focused on data preprocessing, feature transformation, model building, and performance evaluation.
4.1: Data Preprocessing
To make the dataset suitable for machine learning models, several preprocessing steps were applied:

•	Categorical Encoding: Categorical variables such as gender, diet quality, internet quality, parental education level, and part-time job status were converted into numerical form using label encoding. This transformation allowed machine learning algorithms to process non-numeric data effectively.

•	Feature Scaling: Numerical features were scaled using standardization techniques. Feature scaling was especially important for distance-based models such as K-Nearest Neighbors (KNN) and Support Vector Machine (SVM), as these models are sensitive to differences in feature scales.

•	Target Variable Transformation: The continuous target variable, exam score, was converted into categorical classes (Low, Medium, and High performance). This transformation enabled the use of classification algorithms and facilitated accuracy-based performance evaluation.

4.2: Train-Test Split

The dataset was divided into training and testing sets to evaluate model performance on unseen data. A specific test size and random state were selected to ensure a balanced split and reproducibility of results. This approach helped prevent overfitting and provided a fair assessment of each model’s predictive ability.

4.3: Model Selection and Training

Multiple machine learning classification models were trained on the processed dataset to compare their performance:
•	K-Nearest Neighbors (KNN): KNN predicts the class of a student based on the majority class among its nearest neighbors in the feature space.
•	Support Vector Machine (SVM): SVM attempts to find an optimal decision boundary that best separates different performance classes.
•	Decision Tree Classifier: This model creates a tree-like structure of decision rules to classify student performance, making it easy to interpret.
•	Logistic Regression: Logistic regression models the probability of each class using a linear decision boundary
•	Naive Bayes Classifier: Naive Bayes uses probability theory and assumes feature independence. Despite its simplicity, it performed exceptionally well on this dataset.

4.4: Model Evaluation
The performance of each classifier was evaluated using multiple metrics:
•	Accuracy Score: Used to measure the overall correctness of predictions.
•	Confusion Matrix: Provided a detailed breakdown of correct and incorrect predictions for each class.
•	Classification Report: Included precision, recall, and F1-score to evaluate class-wise performance.

A bar chart visualization was used to compare the accuracy scores of all classifiers, enabling easy identification of the best-performing model.

4.5: Comparative Analysis of Models

Upon comparison, it was observed that:
•	All models achieved reasonable accuracy, indicating that the dataset contains strong predictive patterns.
•	Distance-based models such as KNN and SVM performed well after proper feature scaling.
•	Tree-based models captured complex relationships between features effectively.
•	Naive Bayes achieved the highest accuracy among all classifiers, demonstrating its robustness and suitability for this dataset, particularly due to the presence of multiple categorical features.

4.6: Key Findings from Analysis
•	Student performance is influenced by a combination of academic habits, lifestyle factors, and background attributes.
•	Proper preprocessing significantly improved model performance.
•	Simpler probabilistic models like Naive Bayes can outperform more complex models when assumptions align with data characteristics.
Overall, the analysis validated the effectiveness of machine learning techniques in predicting student academic performance and highlighted the importance of model comparison in selecting the best approach.




5.	Conclusion

This project successfully demonstrated the application of exploratory data analysis and machine learning techniques to predict student academic performance using a real-world dataset. By systematically analysing student habits, lifestyle factors, and background information, meaningful insights were derived that highlight the key factors influencing exam performance.

Through comprehensive Exploratory Data Analysis (EDA), the dataset was thoroughly examined to understand data distributions, relationships among variables, and the presence of missing values and outliers. Visualizations such as histograms, boxplots, heatmaps, and count plots played a crucial role in identifying patterns and trends. The EDA process ensured that the dataset was clean, well-structured, and suitable for further analysis.

Following EDA, the dataset was pre-processed through categorical encoding, feature scaling, and target variable transformation. Multiple classification models were trained and evaluated, including K-Nearest Neighbours (KNN), Support Vector Machine (SVM), Decision Tree, Logistic Regression, and Naive Bayes. Each model was assessed using accuracy scores, confusion matrices, and classification reports to ensure a fair and reliable comparison.

Among all the models, the Naive Bayes classifier achieved the highest accuracy, indicating its strong performance on this dataset. Its probabilistic nature and ability to handle categorical features effectively made it particularly suitable for predicting student performance categories. The comparison of multiple classifiers highlighted the importance of selecting an appropriate model based on dataset characteristics rather than model complexity alone.

Overall, this project demonstrates how data-driven approaches can be effectively used to analyse educational data and predict student outcomes. The findings from this study can assist educators and academic institutions in identifying students who may require additional academic support and in developing targeted intervention strategies to improve learning outcomes.


6.	Future scope


The scope of this project can be extended in several ways:
•	Use a larger and more diverse dataset to improve model generalization
•	Apply advanced models such as Gradient Boosting or XGBoost
•	Perform hyperparameter tuning to further improve accuracy
•	Convert the project into a real-time prediction system or web application
•	Include additional features such as socioeconomic factors or learning methods
•	Apply regression models to predict exact exam scores instead of categories


