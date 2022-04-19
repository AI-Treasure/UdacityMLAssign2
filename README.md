# Project 2: Operationalizing Machine Learning

## Table of Content
* [Project Overview](#project-overview)
* [Key Steps](#architectural-diagram)
    * [Authentication](#authentication)
    * [Automated ML Experiment](#automated-ml-experiment)
    * [Deploy the best model](#deploy-the-best-model)
    * [Enable logging](#enable-logging)
    * [Swagger Documentation](#swagger-documentation)
    * [Consume model endpoints](#consume-model-endpoints)
    * [Create and publish a pipeline](#create-and-publish-a-pipeline)
* [Screen Recordin](#screen-recording)
* [Standout Suggestions](#standout-suggestions)

## Project Overview
This is the second project ofthe course Machine Learning Engineer with Microsoft Azure. In this project, we use Azure to configure a cloud-based machine learning production model, deploy it, and consume it. In the second part of this project, we will also create, publish, and consume a pipeline.

In this project, we will follow the steps below:

![](steps.png)

1. **Authentication** : With the Azure machine learning extension, one can create a Service Principal account, needed for the authentication.
2. **Automated ML Experiment** : Here, we will use AutoML to create a best fit model.
3. **Deploy the best model** : The model with the highest accuracy, will be deployed here so that it can be used with API.
4. **Enable logging** : Here we install Application Insights, which is used for logging.
5. **Swagger Documentation** : Swagger will be used to create the documentation for the deployed model.
6. **Consume model endpoints** : Here the endpoint model will be tested to get some predictions for 2 data points.
7. **Create and publish a pipeline** : In the final step, the above is created using a pipeline with the Python SDK.

## Steps

### Authentication
This step was skipped, since I used the Lab provided by Udacity.

### Automated ML Experiment
First, the data set [Bank Marketing data](https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv) was loaded as can be seen below:

![](sample_screenshots/dataset.GIF)
![](sample_screenshots/dataset2.GIF)

Subsequently, Azure's AutoML was used to make a model. 

![](sample_screenshots/automl1.GIF)
![](sample_screenshots/automl2.GIF)

AutoML has ran several runs, and using the accuracy, selected the best performing mode, which was an VotingEnsemble.

![](sample_screenshots/automl3.GIF)
![](sample_screenshots/automl4.GIF)

The voting ensemble had an accuracy of around 95% and was subsequently used for the deployment. 


![](sample_screenshots/deployment1.GIF)
![](sample_screenshots/deployment2.GIF)





