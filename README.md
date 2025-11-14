# FlowQ
This repository contains code for MLOps experiments using DVC for data tracking and MLflow for model management.

## What's MLOps
Building machine learning systems at scale requires more than a notebook and a saved model. You must track parameters, monitor performance, and maintain quality over time. MLOps defines practices that make this process efficient, such as running data processing, training, and evaluation pipelines. Each step contributes a distinct and essential role.

<img width="705" height="311" alt="image" src="https://github.com/user-attachments/assets/9f5a8893-73c7-41b7-ba79-d435b0819cb8" />

The development of an ML system is cyclical, with frequent iteration between steps (source: ML Systems – Chip Huyen).

### DVC
DVC tracks every version of your data. In this project, datasets like `data_00` and `data_01` are combined into `combined_data`, followed by a preprocessed version of the Yahoo Questions dataset.

<img width="320" height="288" alt="image" src="https://github.com/user-attachments/assets/77c4975f-d595-425a-a263-d114a20b4a62" />

### MLflow
MLflow tracks all experiments, making it possible to review metrics, parameters, and model versions through its UI.

<img width="612" height="513" alt="image" src="https://github.com/user-attachments/assets/350aacdd-2a47-40bf-be54-41191f78aed7" />

## NLP

### Exploratory Data Analysis
The initial data exploration included identifying unusual characters, emojis, and missing values. This step helps ensure the dataset is well understood before modeling.

### Modeling
The first model used was **MultinomialNB**, a strong baseline for text classification. Before modeling, the project followed standard NLP steps. Class distribution analysis showed no significant imbalance.

- data cleaning  
- tokenization  
- lemmatization or stemming  

<img width="556" height="435" alt="image" src="https://github.com/user-attachments/assets/4b0696e9-b52d-4203-83b8-985d98513a3a" />

Improving data quality led to better results. The final output included a classification report similar to the one below:

<img width="511" height="359" alt="image" src="https://github.com/user-attachments/assets/9aeba9fc-52aa-4480-b254-008442c7a240" />

The model was built with scikit-learn, and hyperparameters were tuned using GridSearch. Tuning was kept minimal, focusing instead on data quality rather than intensive model tweaking.

## Citation

```
@misc{Carlos2025FlowQ,
  author = {Lima, Carlos},
  title = {FlowQ},
  year = {2025},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/CllsPy/FlowQ}},
}
```

