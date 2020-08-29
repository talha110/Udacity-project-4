 [![Talha110](https://circleci.com/gh/talha110/Udacity-project-4.svg?style=svg)](https://app.circleci.com/pipelines/github/talha110/Udacity-project-4)

# Cloud DevOps Engineer Nanodegree - Machine Learning Microservice API



## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete GitHub repo with CircleCI to indicate that your code has been tested

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

### Running the application

**Setup the Environment:**

```
#Setup a python virtual environment and activate it

python3 -m venv ~/.devops
source ~/.devops/bin/activate

#Install the necessary dependencies
make install

#Linit the Docker file from hadolinter
make lint


```

**Running app.py**

1. Run in Docker: `./run_docker.sh`
2. Run in Kubernetes: `./run_kubernetes.sh`

The application will be running on [http://localhost:8000](http://localhost:8000

### Predict housing prices

While the application is running, run `./make_predicion.sh` to make calls to the API

### Upload Docker image to DockerHub

After running `./run_docker.sh`, execute script`./upload_docker.sh` to upload image to DockerHub
DockerHub Link
[Dockerhub Image Link](https://hub.docker.com/repository/docker/talha110/house_prediction_app

### Kubernetes Steps

- Setup and Configure Docker locally
- Setup and Configure Kubernetes locally
- Create Flask app in Container
- Run via kubectl

### Description of Files  

1. .circleci folder for running builds on circleci.
2. model_data folder containing model files.
3. output text files folder containing outputs text files after running docker and Kubernetes respectively.
4. app.py file containing api code for python
5. Docker file for building docker image
6. Makefile for automating Linux commands
7. bash files for easier execution of multiple Linux commands for running docker , Kubernetes , uploading to docker and making predictions.
