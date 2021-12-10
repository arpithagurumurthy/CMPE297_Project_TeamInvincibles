# Language Modeling using Vertex AI
CMPE 297 - Deep Learning Special Topics Project 

With the rise of social media in recent years, the usage of data for different purposes like election prediction, sentiment analysis, marketing, business, communication has also increased day by day. In this paper we have implemented different language modeling tasks like text classification, sentiment analysis, question answering and summarization. 

## Emotion Classification with Custom Training on Vertex AI

We have achieved the emotion classification by fine tuning the pretrained BERT model and automated all the required steps of the ML system like data collection, model deployment and serving using GCP and Vertex AI.

### Dataset

Emotion from Hugging Face Datasets: 
The dataset contains labels belonging to multiple classes. It is a dataset of Twitter messages with six basic emotions: anger, fear, joy, love and sadness.

### GCP and Vertex AI

**Objective:**
We are custom training the pre-trained BERT based Pytorch model, fine-tuning on various values of hyperparameters and deploying it for emotion classification on the Vertex AI pipeline.

Vertex AI is a unified MLOps platform to help data scientists/ML engineers increase experimentation, deploy faster, and manage models with confidence. It helps build, deploy, and scale ML models faster, with pre-trained and custom tooling within a unified AI platform. 

It is an AI platform that helps in building a unified ML application by integrating Google cloud services. The key features of VertexAI includes:
* A unified UI for the entire ML workflow
* End-to-end integration for data and AI
* Pre-trained APIs for vision, video, natural language, and others
* Support for all open source frameworks

For large datasets and models as in our case, building a training pipeline by leveraging Vertex AI is the most effective method. The training job on Vertex AI is carried out by packaging the code and creating a training pipeline to orchestrate a training job. The 3 steps we have followed are:

*	Packaging the training code as a Python source distribution and submitting the training job to Vertex AI

<img src="" width="400">

*	Hyperparameter training job - We have experimented with hyperparameters such as learning rate and weight decay while fine tuning the BERT model. Below are the results of all the trial runs also showing the best performing model details.

<img src="" width="400">

*	Finally deploying the best model to an endpoint on Vertex AI

<img src="" width="400">

We then serve the fine tuned BERT model predictions on the Streamlit application by using Google Cloud’s ‘aiplatform’ library.

* Below is the screenshot of the model showing predictions for Joy:

<img src="" width="400">

* Below is the screenshot of the model showing predictions for anger:

<img src="" width="400">




