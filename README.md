# Diabetes Prediction Using Ensemble Machine Learning

A machine learning project focused on examining different ensemble-based classification strategies for identifying diabetes across multiple healthcare datasets.

## Project Overview

This repository presents an experimental study of ensemble machine learning approaches for diabetes prediction. Instead of depending on a single classifier, ensemble techniques combine the outputs of multiple learners to obtain more reliable and stable predictions.

Several well-known ensemble strategies are implemented and examined, including **Random Forest, AdaBoost, Gradient Boosting**, and other boosting and stacking-based approaches. Their behavior is investigated using three separate diabetes-related datasets containing different patient characteristics.

### Main Components

* Development of multiple ensemble classifiers for binary diabetes prediction
* Quantitative assessment of the trained models through:

  * Accuracy
  * Precision
  * Recall
  * F1-score
* Exploratory analysis of the available datasets
* Jupyter Notebook implementations accompanied by visual analyses
* Data preparation and transformation procedures
* Training, testing, and comparative evaluation of the machine learning models

The research associated with this project was published in **JMASIF** under the title:

> *Perbandingan Metode Ensemble Learning pada Klasifikasi Penyakit Diabetes*

---

## Software and Libraries

The implementation is based on the following technologies:

* Python
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* LightGBM
* CatBoost

---

## Research Background and Aim

Diabetes mellitus is a chronic disease associated with abnormally high concentrations of glucose in the blood. The increasing prevalence of diabetes has made early identification and risk assessment important areas of healthcare research.

Machine learning can assist this process by learning patterns from patient-related attributes and using those patterns to classify potential diabetes cases.

This study investigates three major ensemble strategies:

1. **Bagging**
2. **Boosting**
3. **Stacking**

The methods are evaluated using three independent datasets:

* **Pima Indians Diabetes Database**
* **Frankfurt Hospital Diabetes Dataset**
* **Sylhet Hospital Diabetes Dataset**

The main purpose is to examine how different ensemble strategies perform when applied to diabetes classification problems involving different datasets.

---

## Data Sources

The experiments use the following publicly available datasets:

1. [Pima Indians Diabetes Database — UCI Machine Learning](https://www.kaggle.com/uciml/pima-indians-diabetes-database)
2. [Frankfurt Hospital Diabetes Dataset — John](https://www.kaggle.com/johndasilva/diabetes)
3. [Sylhet Hospital Diabetes Dataset — Ishan Dutta](https://www.kaggle.com/ishandutta/early-stage-diabetes-risk-prediction-dataset)

---

## Experimental Procedure

The project follows a series of stages to prepare the data and evaluate the classification models.

### 1. Data Preparation

The original datasets are processed before being supplied to the classifiers.

A `MinMaxScaler` is applied so that numerical attributes are transformed to a common scale between **0 and 1**.

### 2. Exploratory Analysis

The datasets are examined to understand their characteristics, distributions, and relationships between available features.

### 3. Feature Processing

Relevant attributes are prepared for use in the classification process, followed by the necessary feature engineering operations.

### 4. Train-Test Division

Each dataset is divided into two subsets:

* **80%** for model training
* **20%** for model testing

### 5. Classifier Construction

The selected ensemble algorithms are configured and implemented using the processed datasets.

### 6. Model Training and Prediction

The classifiers are trained with the training subset and subsequently used to generate predictions for unseen testing data.

### 7. Evaluation

Model performance is measured using four classification metrics:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-score**

---

## Ensemble Strategies

The implemented methods can be grouped into three main ensemble families.

|               Bagging               |                Boosting               |                Stacking               |
| :---------------------------------: | :-----------------------------------: | :-----------------------------------: |
| ![Bagging](images/1.%20Bagging.jpg) | ![Boosting](images/2.%20Boosting.jpg) | ![Stacking](images/3.%20Stacking.jpg) |

### Bagging-Based Models

The bagging category contains:

* Bagging Classifier
* Random Forest
* Extra Trees

These approaches construct multiple learners and combine their predictions to reduce model variance and improve generalization.

### Boosting-Based Models

The boosting experiments include:

* Adaptive Boosting
* Gradient Boosting
* Extreme Gradient Boosting
* Light Gradient Boosting
* CatBoost

Boosting methods sequentially construct a collection of learners, with subsequent models attempting to improve upon errors made by earlier ones.

### Stacking

The stacking experiment uses:

* Stacked Generalization

In stacking, predictions generated by several base learners are combined and supplied to another model that produces the final classification result.

---

## Accuracy Results

### Pima Indians Diabetes Database

![Accuracy results for Dataset 1](images/Grafik%20Akurasi_Dataset%201.png)

### Frankfurt Hospital Diabetes Dataset

![Accuracy results for Dataset 2](images/Grafik%20Akurasi_Dataset%202.png)

### Sylhet Hospital Diabetes Dataset

![Accuracy results for Dataset 3](images/Grafik%20Akurasi_Dataset%202.png)

---

## Findings

The experimental results indicate that boosting-based classifiers achieve strong classification performance across the evaluated datasets.

Among the examined approaches, **Light Gradient Boosting** produces the highest accuracy in most of the experiments, particularly for the Frankfurt Hospital and Sylhet Hospital datasets.

The results demonstrate that ensemble techniques can behave differently depending on the characteristics of the dataset. Therefore, model performance should be assessed separately for each dataset rather than assuming that one ensemble strategy will always produce the same outcome.


---

## Contributors

* [Linggar Maretva Cendani](https://github.com/LinggarM) — [linggarmc@gmail.com](mailto:linggarmc@gmail.com)
* Adi Wibowo — [bowo.adi@live.undip.ac.id](mailto:bowo.adi@live.undip.ac.id)

---

## License

The source code is distributed under the **MIT License**.

Refer to the [`LICENSE`](LICENSE) file included in this repository for the complete license terms.

---

## Data Acknowledgments

The datasets used in this work were obtained from the following sources:

* [UCI Machine Learning — Pima Indians Diabetes Database](https://www.kaggle.com/uciml/pima-indians-diabetes-database)
* [John — Diabetes Dataset](https://www.kaggle.com/johndasilva/diabetes)
* [Ishan Dutta — Early Stage Diabetes Risk Prediction Dataset](https://www.kaggle.com/ishandutta/early-stage-diabetes-risk-prediction-dataset)
