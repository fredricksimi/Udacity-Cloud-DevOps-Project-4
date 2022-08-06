[![CircleCI](https://circleci.com/gh/fredricksimi/Udacity-Cloud-DevOps-Project-4.svg?style=svg&circle-token=<YOUR_STATUS_API_TOKEN>)](<LINK>)


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

## Setup the Environment

* Create a virtual environment with Python 3 and activate it. 
```bash
python3 -m venv ~/.devops
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`
4. Make predictions: `./make_prediction.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

### The Files included:

* `.circleci` - circleci configuration script
* `model_data` - ML model data (model, csv data)
* `output_txt_files` - The project output files (docker, kubernetes)
    * `docker_out.txt` - run_docker.sh output
    * `kubernetes_out.txt` - run_kubernetes.sh output
* `app.py` - python web application entry point file
* `Dockerfile` - docker image config
* `make_prediction.sh` - make prediction HTTP call script
* `Makefile` - make file (install, test, lint steps)
* `requirements.txt` - web application dependencies (python, libraries)
* `run_docker.sh` - run docker container script
* `run_kubernetes.sh` - run kubernetes pod for the web app script
* `upload_docker.sh` - upload docker image to dicker hub script