# Early Sepsis Prediction 6 Hours Prior to onset

![alt text](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTPtbufUSQ4xfdWG4uzqbZENOFsZhkbjDLanbqnWuQP2KCU-M_7YxqPkb5d1C_UabK-JJ4&usqp=CAU)


# Introduction 
Sepsis is a critical medical condition that occurs when the body’s immune system responds aggressively to an infection, potentially causing damage to its own tissues and organs. This can lead to long-term health complications and, in severe cases, death.

This repository contains a Jupyter Notebook that demonstrates a machine learning approach to predict whether a patient is likely to develop sepsis within the next six hours. The notebook explores various techniques to build the most accurate predictive model.

The primary objective is to classify patients into one of two categories:

 0 = Sepsis will not occur.

 1 = Sespsis will occur.

# Dataset Information
This project utilizes the MIMIC-IV dataset, which includes extensive clinical data from patients in emergency and intensive care units. The dataset provides a strong foundation for developing models aimed at early sepsis prediction.

Link to the Dataset : https://physionet.org/content/mimiciv/3.1/


# Methodology
## 1. Research / Understanding the problem statement.

* **Objective:** To gain industry spesific insights and a deeper understanding of the causes and effects of sepsis.

A genereal reseach on sepsis majorly reseaching on its causes, adverse effects, and progression. This understanding has helped me gain deeper insights into the data and its relevance to the disease.

## 2. Data Extraction.

* **Ojbective:** Extract all the essential features.

Selective columns that may provied the machine learning model with a advantagious ability to predict sepsis were extracted. The total size of the datasbase was 40gb and the extracted data that was extarcted using various techniques such as incremental extraction and extarction using temporary files had a resusltant file of 1gb.


## 3. Pre-Processing the Data.

* **Ojbective:** Clean the data impute missing data, remove outliers and imporove the predictive power of the model using esentail features. 

Both the training and testing datasets have been preprocessed using consistent techniques to ensure data integrity and model reliability. For categorical variables, missing values were not present and lable encoding was applied for feature encoding.

For numerical features, missing values were imputed using an Iterative Imputer. Additionally, the outliers were not removed as the abnomaities present in the data provied the model will strong indications of the onset of sepsis in the future.

## 4. Building a models that predict if patients will contract sepsis.

* **Ojbective:** Build models.

For machine learning models, XGBoost and a Ensemble Model (Random Forest, Naive Bayes and K-Nearest Neighbours) were employed due to their robustness and ability to handle complex, non-linear relationships. 

## 5. Model Optimization & Model Explainability

* **Ojbective:** Optimize the models hyperparameters.

BayesSearch was used for the hyperparameter optimization to improve the model performance and 5 fold cross validation was used to imporve the models ability to genrealize to new unseen data.

# Requirements
* Python 3.x
* Jupyter Notebook
* Pandas
* Matplotlib
* Seaborn
* XGboost
* Sklearn
* Imblearn
* Fastai
* Skopt
* Joblib

# Installation
```
pip install pandas matplotlib seaborn scikitlearn imblearn fastai skopt joblib
```

# Conclusion
This project demonstrates the potential of machine learning in predicting sepsis up to 6 hours before onset, which can enable timely medical intervention. The best-performing model XGboost has achieved an accuracy of 85% and the ensemble model (Random Forest, Naive Bayes and K-Nearest Neighbours) has achieved an accuracy of 81%, showing promise for use in clinical decision support systems.
  
