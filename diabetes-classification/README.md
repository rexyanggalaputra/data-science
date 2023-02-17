# Diabetes Classification
## Business Understanding
* Diabetes is a chronic disease characterized by high blood sugar (glucose) levels. Glucose is the main energy source for the cells of the human body. Glucose that accumulates
in the blood due to not being absorbed by the body's cells properly can cause various disorders of the body's organs. If diabetes is not controlled properly, various complications can arise that endanger the patient's life. Early detection of diabetes is important so that it can be handled properly and does not cause adverse effects on the human body.

* Objective : Classification
* Benefit   : Assist the medical team in providing early identification of individuals who may have diabetes.

## Data Understanding
* This dataset is originally from the National Institute of Diabetes and Digestive and Kidney Diseases. The objective of the dataset is to diagnostically predict whether or not a patient has diabetes, based on certain diagnostic measurements included in the dataset.

* The dataset consist of 390 rows and 17 columns taken from [Kaggle](kaggle.com) platform. Predictor variables includes the number of pregnancies the patient has had, their BMI, weight, age, glucose, and so on.

* [Source Data](https://www.kaggle.com/houcembenmansour/predict-diabetes-based-on-diagnostic-measures)

* Data Dictionary
  - patient_number    : Patient id number
  - cholesterol       : Cholesterol levels of patient
  - glucose           : Sugar level of patient
  - hdl_chol          : High-Density-Lipoprotein (HDL) cholesterol
  - chol_hdl_ratio    : High-Density-Lipoprotein (HDL) cholesterol ratio
  - age               : Age of patient
  - gender            : Gender of patient
  - height            : height of patient
  - weight            : Weight of patient
  - bmi               : Body Mass Index of patient
  - systolic_bp       : Systolic blood pressure
  - diastolic_bp      : Diastolic blood pressure
  - waist             : Waist of patient
  - hip               : Hip of patient
  - waist_hip_ratio   : Waist-to-hip ratio (WHR)
  - diabetes          : Is patient have diabetes or not

## Data Preparation
* Code Used      : Jupyter Notebook
* Library(es)    : Pandas, Numpy, Matplotlib, Seaborn, Scikit-Learn
* Dataset Overview

![df ov](https://user-images.githubusercontent.com/85033777/144693773-be5c9644-575c-474c-952d-dd91a2106d57.png)

* Checking Missing Value

![p3 df info](https://user-images.githubusercontent.com/85033777/144651240-be7a6316-a147-46b8-a494-5cdcbdfce767.png)

Table above says that all columns consist of full 390 data. It means there are no missing value for all columns, so the process can be continued.

* Scaling

Scaling is used to normalize the data because in the dataset column there are differences in the numerical scale units.

![scaling](https://user-images.githubusercontent.com/85033777/144687147-7a55196a-6dc5-4862-9010-d0aea4af4970.png)

* Splitting data

In this case, I'm going to split the data into 10% for test and 90% for training. It means there are 39 data are in test size and 351 data are in training size.

## Modelling

In this processs I'm trying to use 4 model, they are K-Nearest Neighbors, Decision Tree, SGD Classifier, and Logistic Regression. Here I add Principal Component Analysis for each model and applying paraameter tuning using Pipeline and GreadSearchCV. For more details, you can look in the [source code](https://github.com/rexyanggalaputra/Diabetes-Classification/blob/main/Projek%203%20Klasifikasi%20Penyakit%20Diabetes.ipynb). The results are shown as below :

* K-Nearest Neighbors

![knn est](https://user-images.githubusercontent.com/85033777/144692745-6cae2ef1-fa20-4d55-9990-4c249e70026a.png)

![knn conf](https://user-images.githubusercontent.com/85033777/144692683-226b2ae8-568f-4913-a308-999c33f5076c.png)

* Decision Tree

![dt est](https://user-images.githubusercontent.com/85033777/144692743-63b8ea4c-d172-481b-b7e3-d5b452bc4c3e.png)

![dt conf](https://user-images.githubusercontent.com/85033777/144692682-4c9daab6-d6a5-4948-a6df-4aa3c2936288.png)

* SGD Classifier

![sgd est](https://user-images.githubusercontent.com/85033777/144692749-67884295-3cc0-4617-8b2b-6c7eedb824cc.png)

![sgd conf](https://user-images.githubusercontent.com/85033777/144692681-b369da63-f566-474e-9247-e7277fc38658.png)

* Logistic Regression

![lr est](https://user-images.githubusercontent.com/85033777/144692746-9415cf2d-5932-4789-b827-5e4d2dfd1d45.png)

![lr conf](https://user-images.githubusercontent.com/85033777/144692680-1f47bc68-d89d-4ae4-a602-1aeb8aa8c3bd.png)

## Evaluation
Evaluate the model using Accuracy, Recall, and Precision

![akurasi](https://user-images.githubusercontent.com/85033777/144692742-c4f54bd6-32fc-4eef-9cca-ec583c82d81d.png)

![recall presisi](https://user-images.githubusercontent.com/85033777/144692747-db17ef43-7fbd-45d1-883f-10131ca170f0.png)

![all ressult](https://user-images.githubusercontent.com/85033777/144692678-0702ae90-3273-4af0-85ec-9c3576ca4be2.png)

## Summary
From the several models above, we can se that Logistic Regression is the best model among the four models that have been made. The Logistic Regression model shows the Training Accuracy value is 0.923077 and Test Accuracy value is 0.948718, it shows that the model does not occur overfitting and the model has an accuracy of 95% to predict. Then the matrix considered is Recall. Recall from the Logistic Regression model has the highest number, which is 0.888889, so this model is the best compared to the others. 
