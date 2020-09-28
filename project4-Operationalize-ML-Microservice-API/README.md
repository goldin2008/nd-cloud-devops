<include a CircleCI status badge, here>

[![<CircleCI>](https://circleci.com/gh/goldin2008/project-ml-microservice-kubernetes.svg?style=svg)](https://circleci.com/gh/goldin2008/project-ml-microservice-kubernetes)

> https://circleci.com/docs/2.0/status-badges/

> https://nf-co.re/errors

Great Assignment! You really showed up you competence on deploying a ML-Model to docker and kubernetes. Perhaps you also want to try Heroku - a platform for serverless applications: www.heroku.com
Here ist a blog-post describing how to deploy a ML model with flask/starlette on Heroku: 
> https://medium.com/analytics-vidhya/put-deep-learning-image-classifier-in-action-a956c4a9bc58


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
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

### Files

* `README.md`: Readme file for the GitHub repository
* `.circleci` - circleci config scripts
* `config.yml` - Checks the project code for errors with CircleCI
* `app.py`: Main Python file for the flask application
* `Dockerfile`: Dockre configuration file for creating the docker image
* `Makefile`: Make file that includes the command to install the python dependencies (`make install`) and linting (`make lint`)
* `requirements.txt`: list of the dependency libraries required by the app
* `run_docker.sh`: shell script to build, list and run the docker container
* `upload_docker.sh`: shell script to tag and upload the docker image to Docker Hub
* `run_kubernetes.sh`: shell script to run the container in a Kubernetes pod, list the pod and forward its port to the host port
* `make_prediction.sh`: Shell script to call the application endpoint with test data
* `model_data` - ML model related data (model, csv data)
* `output_txt_files` - project output files (docker, kubernetes)
    * `docker_out.txt` - run_docker.sh output
    * `kubernetes_out.txt` - run_kubernetes.sh output
    
---

## Setup the Environment

* Create a virtualenv and activate it

```sh
python3 -m venv ~/.devops
source ~/.devops/bin/activate
```

* Run `make install` to install the necessary dependencies

---

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`
4. Make predictions: `./make_prediction.sh`

### Docker

1. Publish docker image: `./upload_docker.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

### Kubernetes Clean Up
- `kubectl delete deployment.apps/development`
- `kubectl delete svc development`

---

### References
'''
> https://github.com/StephanStu/Operationalization-of-a-Machine-Learning-Microservice-API

> https://github.com/henokhm/udacity-cloud-devops-project-4

> https://github.com/DavidBertrand/udacity-project-ml-microservice-kubernetes

> https://github.com/kickertw/UdacityDevOpsProj5

> https://github.com/Sarony11/Udacity-DevOps-Project5

> https://github.com/trajkd/project-ml-microservice-kubernetes/blob/master/README.md
'''
