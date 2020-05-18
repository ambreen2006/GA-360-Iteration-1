# GA-360-Iteration-1
This is analysis for a blog project required in Udacity Data Scientist Nanodegree. It uses freely available data from Google Open Datasets.

CRISP-DM process followed is documented below

## Dataset 

As described above the merchant store data is obtained from: 
https://console.cloud.google.com/marketplace/details/obfuscated-ga360-data/obfuscated-ga360-data?filter=solution-type:dataset&filter=category:analytics&id=45f150ac-81d3-4796-9abf-d7a4f98eb4c6

The notebook `Google Analytics Sample Big Query.ipynb` contains the big query used for downloading the data which is then saved to CSV.

The big query requires pre-setup and installation of several packages.

## Data preparation

* NaN's are tranformed
* All NaN's columns and rows are dropped.
* Categorical data is transformed to dummy variables
* Data frame is normalized
* Unbalanced data is undersampled

## Analysis and Modeling 

Analysis sought to answer the following questions:

* Where are the buyers from?
* What kind of platform or technology the buyers are using?
* Can we build a classification model to distinguish between a potential buyer or a window shopper?

Classification model is created using:

* RandomForestClassifier
* AdaBoostClassifier
* GaussianNB
* RandomForestClassifier with non-default parameters

## Evaluation

The models are evaluated based on:

* F-1 score on test and train data 
* Recall
* Precision