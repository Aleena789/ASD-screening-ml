# ASD-screening-ml
Autism screening classification using Machine Learning
Overview:
This projects builds a classifier to predict Autism Spectrum Disorder. This dataset is imbalanced (fewer ASD cases compared to non-ASD), standard accuracy alone is not a reliable metric. Instead, we emphasize metrics such as precision, recall, F1-score, and Average Precision (AP) to evaluate the models fairly.

To be noted: This is a educational project only and not intended for clinical or diagnostic use.

Data Overview
- Dataset contains 14 features +1 target ('Class')
- Features: A1-A10(binary, age,sex,jaundice,family_asd(categorical)
- Target: Class(Yes= Autism, no= no autism)

Methodology

Exploratory Data Analysis (EDA):
 -Explored the screening features and the dependencies between the features.
 -Visualized class imbalance.
 -Identified potential predictors (all of them were important).

Data Preprocessing
 -No missing values.
 -Encoded categorical variables.
 -Attempted random oversampling to balance classes, but found it led to potential overfitting. Final results are reported without oversampling for fairness.

Modeling
 -Trained multiple classifiers (Logistic Regression and Random Forest).
 -Evaluated using precision, recall, F1-score, Average Precision and PR curves.

Evaluation Metrics
 -In healthcare settings, false negatives (failing to detect ASD) can be more harmful than false positives.
 -Precision & Recall provide better insight than accuracy alone.
 -F1-score (harmonic mean of precision and recall) balances both.
 -Average Precision (AP) summarizes the area under the Precision-Recall curve.

Visualizations included
 -Classification report and PR curve of both the classifiers in the graphs and report folder.

Result
 -Logistic Regression being the baseline model still had an AP of 0.97 indicating simple models are effective.
 -Random Forest achieved an AP of 0.99 showing ability to detect asd while having high precision.
 -to be noted: such high results might be due to overfitting

-Limitations
 -Dataset is small and imbalanced.
 -The dataset might not be diverse enough.

Further improvemnts:
 -try additonal models
 -collect more diverse data.

-All steps from EDA to model training and evaluation, are included in the ASD_screening.ipynb notebook.
-For detailed visualisation please refer to the notebook.
