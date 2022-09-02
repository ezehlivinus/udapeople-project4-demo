[![CircleCI](https://dl.circleci.com/status-badge/img/gh/ezehlivinus/udapeople-project4-demo/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/ezehlivinus/udapeople-project4-demo/tree/main)


## Project Overview

In order to operationalize a Machine Learning Microservice API for this project, I used the skills I learned in the course.

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Purpose
- Invoke a Docker container
- Place the container in a public registry (hub.docker.com)
- Utilize a Kubernetes cluster to run the deployed application.
- Use CircleCI to integrate for continuous integration.

## Dependencies
 - [Python 3.7](https://www.python.org/downloads/)
 - [Hadolint](https://github.com/hadolint/hadolint)
 - [Docker](https://www.docker.com/)
 - [Kubernetes(minikube)](https://minikube.sigs.k8s.io/docs/start/)
 - 
 
## Usage and files
 - Most things are terminal commands and 
 - long commands has been moved to shell script file whith `.sh` extension.
 - Examples: 
   - `run_docker.sh`
   - `make_prediction.sh` which contain a `curl` command that can make a POST 
   request to local instance of the app send along json data to be used for the prediction
   - `Makefile` with no extension, is a special file, containing shell commands.
 - clone the repo: `git clone git@github.com:ezehlivinus/udapeople-project4-demo.git`
 - navigate to the project directory: `cd git clone udapeople-project4-demo`
 - setup the environment:
   - On your terminal run: `make setup`
 - Install dependencies using `make` by running the following on your terminal
   - `make setup`
 - You may lint: `make lint`
 - Run the application using docker: `./run_docker.sh`

## Uploading to your docker hub account
You can do this with the script file `./upload_docker.sh`. 
we make an environment to keep our username and desired image.

 - Locate the following line of code in the script:
   ```dockerpath=ezehlivinus/udapeople```
 - Chnage `ezehlivinus` to your docker hub username
 - Change `udapeople` to your prefered image name
 - In essence: the code syntax is: `dockerpath=your-docker-hub-username/image-name`
 - If you changed the user and the image name
   - You may want to do the same by changing the same code on this file: `./run_kubernetes.sh` as you will be using next


## Deployment
The script file `./run_kubernetes.sh` contain the code run the deployment to kubernetes
 - Note: deploy as your own project, 
 - Run the following command to deploy: `./run_kubernetes.sh`
 
<!--* Run `make install` to install the necessary dependencies-->

<!--### Running `app.py`-->

<!--1. Standalone:  `python app.py`-->
<!--2. Run in Docker:  `./run_docker.sh`-->
<!--3. Run in Kubernetes:  `./run_kubernetes.sh`-->

<!--### Kubernetes Steps-->

<!--* Setup and Configure Docker locally-->
<!--* Setup and Configure Kubernetes locally-->
<!--* Create Flask app in Container-->
<!--* Run via kubectl-->
