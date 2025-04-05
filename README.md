## Problem Statement

Can we leverage Kaggle Airbnb data (https://www.kaggle.com/datasets/vrindakallu/new-york-dataset) to predict Host metrics using XGBoost. Specifically, can we predict a top rated host (rating >= 4.8) given listing features?

## Model Results

After retreiving optimal hyperparameters via a Grid Search, the model yields fairly strong results.

<img src="https://github.com/mwheeler235/ny-airbnb-2024/blob/main/img/confusion matrix.png" width="600" height="450">

The top features associated with predicting a high rated host:

<img src="https://github.com/mwheeler235/ny-airbnb-2024/blob/main/img/top features.png" width="600" height="450">

## Conclusion

* With resulting Accuracy = 62.2% and Recall = 92.2%, this model is effective at catching most of the Top Rated hosts, but also overdiagnoses leading to a high false positive rate (FP/(FP+TN)) = 1146/(1146+456) = 71.5%
* Reducing false positives will be difficult given the limited data scope and features
* However, it is impactful that we can achieve a F1 Score of 72.1% when predicting a high rated host (rating >= 4.8) given corresponding property features
