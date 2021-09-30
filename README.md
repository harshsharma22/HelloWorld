# HelloWorld

A Basic Simple CI/CD solution using github action which deploy a nodejs application on kubernetes on every push on branch main

## Imporant File

**DOCKERFILE** :- This file creates a docker image of our nodejs application\
**DOCKER-COMPOSE.YML** :- This file defines our application as contianer

## UTilities Used Inside Github Actions

action/checkout@v2 :- This action is used to checkout the current repo\
action/setup-node@v2 :- Setup up nodejs\
kompose :- Converts docker-compose file to kubernetes yml file\
steebchen/kubectl@v2.0.0 :- This action uses kubectl as utility


## Usage
This Project Contains a basic **HELLO WORLD** nodejs application that runs on port 3000\
The **CI/CD** workflow contains 3 job which run on every push on main branch\
jobs:-\
  1:- lint job : This Job check for the lint error in our nodejs application\
  2:- build job: This Job creates and pushes image into docker hub registry.\
  3:- build-deploy: This job deploy built image to the kubernetes when a push happens on main branch.\
**NOTE:- KUBECONFIG file should be converted to base64**

## Steps Followed

1:- Created  a github respository\
2:- Created a basic nodejs application that runs a HTTP server and greet with Hello World\
3:- Setup github action to deploy application to kubernetes\
4:- Created k3s  cluster\
5:- Copied kubeconfig file as base 64 formatted string and pasted in new Github repository secret named NONPROD_KUBE_CONFIG

## Components Used

1:- Nodejs\
2:- Github Actions\
3:- K3s Kubernetes
