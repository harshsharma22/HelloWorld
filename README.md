# HelloWorld

A Basic Simple CI/CD solution using github action which deploy app on kubernetes on every push on branch main

## Imporant file

**DOCKERFILE** :- this file create a docker image of our nodejs application 
**DOCKER-COMPOSE.YML** :- this file define our application as contianer

## UTILITIES USED INSIDE GITHUB ACTIONS

action/checkout@v2 :- this action used to checkout the current repo
action/setup-node@v2 :- setup up nodejs 
kompose :- convert docker-compose file to kubernetes yml file
steebchen/kubectl@v2.0.0 :- this action uses kubectl as utility


## Usage
This Project Contain a basic **HELLO WORLD** nodejs application runs on port 3000
The **CI/CD** contain 3 job which run on every push on main branch
jobs:-
  1:- lint job : this Job check for the lint error in our  nodejs application
  2:- build job: this Job create and push image onto docker hub. 
  3:- build-deploy: this job deploy build image to the kubernetes when there a push happens on main branch.
**NOTE:- KUBECONFIG file should be convert to base64 **

## Steps followed

1:- created  a github respository
2:- created a basic app to return Hello World
3:- setup github action to deploy app to kubernetes
4:- create k3s  cluster
5:- copy kubeconfig file to base 64  format

## Components Used

1:- Nodejs
2:- Github Actions
3:- K3s Kubernetes
