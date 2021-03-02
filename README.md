# Operationalizing Machine Learning on Azure

# Overview

This project demonstrates how to apply MLOps principles in Azure. MLOps stands for machine learning operations and it is the art of applying DevOps principles in machine learning such as deploying a model, consuming endpoints and automating a pipeline.

In this project, we work with a bank marketing dataset to accurately predict if a potential client will subscribe to the bank's term deposit. A model is created using AutoML, and the model is then deployed and consumed via a REST endpoint.

# Architectural Diagram

![Workflow](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/workflow.png)

(Workflow Taken from Udacity)

# Key Steps

## Authentication

There was no need to authenticate as i used the environemnt provided by Udacity where authentication was already implemented.

## AutoML model

### Dataset Used

As mentioned earlier, we used the bank marketing dataset in this project.

![dataset](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/dataset.png)

### Completed Experiment

We create an AutoML run on this dataset to solve a classification problem while explaining the best model.

![completed_experiment](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/automl_complete.png)

### Best Model

The best model was a Voting Ensemble model with an accuracy of 92%

![best_model](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/best_model.png)

## Deploy the Best Model

The voting ensemble model was then deployed

![deploy_model](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/deploy_model.png)

## Enable Logging

After deploying the best model, Application Insights was enabled and the logs were retrieved

![logs](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/logs.png)

## Consume Model Endpoint

### Swagger

Swagger is a tool that displays the contents of an API in easy to read manner. The images below showsSwagger running on the localhost and the responses of the model

![swagger_1](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/swagger_1.png)

![swagger_2](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/swagger_2.png)

![swagger_3](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/swagger_3.png)

### Endpoint

The interact with the deployed model we use the endpoint.py script

![endpoint](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/endpoint.png)

### Benchmark

![benchmark](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/benchmark.png)

## Create and Publish a Pipeline

### Create Pipeline

The first step is to create a pipeline

![pipeline_run](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/pipeline_run.png)

The pipeline endpoint

![pipeline_endpoint](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/pipeline_endpoint.png)

Dataset Used

![pipeline_dataset](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/pipeline_dataset.png)

### Publish Pipeline

![pipeline_publish](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/pipeline_publish.png)

![pipeline_rundetails](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/pipeline_rundetails.png)

In the published pipeline overview we can see the status (ACTIVE) and a REST endpoint

![pipeline_active](https://github.com/adhamalhossary/operationalizing-ml-on-azure/blob/main/screenshots/pipeline_active.png)

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:
