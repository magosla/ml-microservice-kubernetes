## CircleCI Run status
[![CircleCI](https://dl.circleci.com/status-badge/img/gh/magosla/ml-microservice-kubernetes/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/magosla/ml-microservice-kubernetes/tree/main)

## Project Summary
This project applies the skills acquired in this course to to operationalize a Machine Learning Microservice API. 
Using the given pre-trained `sklearn` model model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.
The application was built and deployed to docker hub

## Running the application locally
* Install Docker
* Build container: execute `bash run_docker.sh` on the terminal. This shell script run all the commands needed to build and run the docker image
* Making predictions? execute `bash make_prediction.sh` on the terminal. This shell script sends a POST request to the running application to get predictions of housing prices.

## Running the application on a Kubernetes cluster
* Install Kubernetes and Minikube
* Start Minikube by executing `minikube start`
* Create a Kubernetes pop: execute `bash run_kubernetes.sh` on the terminal. This script runs a command to create a pod with an image from Docker hub, and forwards the container port to 8000
* With the container running:
* * Making predictions? execute `bash make_prediction.sh` on the terminal. This shell script sends a POST request to the running application to get predictions of housing prices.


## Repository Files
* Folder `output_txt_files/` contains files with output from running the following scripts `run_docker.sh` and  `make_prediction.sh`
* Folder `screeshots/` contains screeshots of output from completing task 3 and task 6