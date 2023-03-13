# modeling_nepal_earthquake_damages

# Table of Content

1. [Project Motivations](#project-motivations)
1. [Datasets](#datasets)
1. Files
1. Results
1. Acknowledgment

## Project Motivations

![image](</images/1600px-2015_Earthquake_in_Nepal-Pashupatinath_Temple_Area_(12).JPG>)
credibility of photo: [Wikimedia Commons](<https://commons.wikimedia.org/wiki/File:2015_Earthquake_in_Nepal-Pashupatinath_Temple_Area_(12).JPG>)

In 2015,a heavy earthquake with a magnitude of 7.8 struck Nepal. This earthquake is also called Gorkha earthquake caused a severe annihilation on major city buildings and properties. The objective of this project is to predict the level of damage to buildings caused by this earthquake.

## Datasets

The data was collected through surveys by [Kathmandu Living](https://kathmandulivinglabs.org/) Labs and the [Central Bureau of Statistics](https://cbs.gov.np/), which works under the National Planning Commission Secretariat of Nepal. This survey is one of the largest post-disaster datasets ever collected, containing valuable information on earthquake impacts, household conditions, and socio-economic-demographic statistics.

## Files

- **earthquake_damages.ipynb**: jupyter notebook for ETL and modeling
- **submission_format.csv**: submission format file
- **submission.csv and submission.csv**: files containing level of damage predictions on buildings caused by earthquake
- **test_values.csv**: test datasets
- **train_values.csv**: train datasets
- **train_values.csv**: labels for the train datasets

## Results

The feature varibles contain categorical features (string type) which was convert to numerical variables and imbalance effect on the multi class labels was balanced with Synthetic Minority Oversampling Technique (SMOTE). The evaluate metric is F1 score which balances the precision and recall of a classifier. Traditionally, the F1 score is used to evaluate performance on a binary classifier, but since we have three possible labels we will use a variant called the `micro averaged F1 score`.
![image](/images/Screenshot%202023-03-13%20at%2018.22.53.png)
where, **TP** is True Positive, **FP** is False Positive, **FN** is False Negative, and krepresents each class in 1,2,3.

The classifier model (RandomForestClassifier) with hyperparameters tuning gave F1 score of **81%**.

## Acknowledgment

Thanks to [drivendata](https://www.drivendata.org/competitions/) for the opportunity to conduct this project and provision of the dataset through [Central Bureau of Statistics](https://cbs.gov.np/) which make this project possible.
