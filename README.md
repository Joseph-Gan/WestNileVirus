# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Kaggle Competition - Starter

## Background


West Nile Virus(WNV) is usually spread to humans through infected mosquitos. Around 20% of individuals who become infected with the virus develop symptoms ranging from a persistent fever, to serious neurological illnesses that can result in death.

In 2002, Chicago recorded it's first human incident of West Nile virus. By 2004 the City of Chicago and the Chicago Department of Public Health (CDPH) had built a comprehensive surveillance and control program that is still in effect today.

Every week from late spring through the fall, mosquitos in traps across the city are tested for the virus. The results of these tests influence when and where the city will spray ariel pesticides to reduce adult mosquito populations. Every week from Monday through Wednesday, these traps collect mosquitos, and the mosquitos are tested for the presence of West Nile virus before the week ends. The test results include the number of mosquitos, the mosquitos species, and whether West Nile virus is present in the cohort.

This project is from: https://www.kaggle.com/c/predict-west-nile-virus/overview.

## Business Problem

Due to a recent outbreak of the West Nile Virus in the city of Chicago, the Data Science team at the Disease and Treatment Agency has been tasked by the Centers for Disease Control (CDC) to develop a strategy to deploy the effective use of pesticides. Targeting spraying efforts to areas of high risk will help to mitigate future outbreaks.

Leveraging on weather, location, mosquito population and spraying data, we will build a binary classification model that predicts the presence of the West Nile Virus in the city of Chicago. The model that achieves the highest ROC AUC score on the validation set, will be selected as our production model. The model is also expected to outperform the baseline ROC AUC score of 0.5. A cost-benefit analysis will also be done to determine if the benefits of spraying outweighs its costs.

## Executive Summary

Out of all the classification models built, XGBoost was selected as it achieved the highest ROC AUC score on the validation set. The model attained an ROC AUC of 0.84 on the validation set, outperforming the baseline score of 0.5. As observed from the model's feature importance, it turns out that seasonality plays a very key role in mosquito breeding and the spread of WNV, with 'month' being the most important predictor. Besides other sesonality features like 'week' and 'day', 14-day rolling weather conditions like wetbulb, dewpoint and temperature are also key in predicting the presence of WNV in the City of Chicago. The model received a 0.78 ROC AUC score on Kaggle.

Based on the cost benefit analysis, for worst case scenario, spraying with more than 16 WNV cases overweighs the cost of the spray.

As the model performs relatively well on unseen data, the Disease and Treatment Agency will now be able deploy pesticide-spraying efforts to areas of high risk. An efficient allocation of resources will help help to clamp down on the WNV outbreak, reducing residents' exposure to the virus

## Dataset

The dataset, along with description, can be found here: [https://www.kaggle.com/c/predict-west-nile-virus/](https://www.kaggle.com/c/predict-west-nile-virus/).

## Methodology Summary

![alt text](https://github.com/Joseph-Gan/WestNileVirus/asset/blob/main/Flowchart.jpg?raw=true)
