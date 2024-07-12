


# deep_learning_kidney_disease

**Workflows

=============================================
Update config.yaml

**Update secrets.yaml [Optional]-for users,database users

Update params.yaml

Update the entity

Update the configuration manager in src config

Update the components

Update the pipeline

Update the main.py

Update the dvc.yaml

app.py**

=======================================================
**********
Documentation

MLflow tutorial

cmd
mlflow ui
dagshub
dagshub

MLFLOW_TRACKING_URI=https://dagshub.com/gmsahu/deep_learning_kidney_disease.mlflow
MLFLOW_TRACKING_USERNAME=xxxxx
MLFLOW_TRACKING_PASSWORD=d93fec23a362688182f3ae34481fdbb98f4056b9
python script.py

Run this to export as env variables:

export MLFLOW_TRACKING_URI=https://dagshub.com/gmsahu/deep_learning_kidney_disease.mlflow

export MLFLOW_TRACKING_USERNAME=xxxxxx 

export MLFLOW_TRACKING_PASSWORD=0fc407aa5dfc04d23a42976570fee78f40774e40
============================================================================
DVC cmd
dvc init
dvc repro
dvc dag
About MLflow & DVC
MLflow

Its Production Grade
Trace all of your expriements
Logging & taging your model
DVC

Its very lite weight for POC only
lite weight expriements tracker
It can perform Orchestration (Creating Pipelines)
AWS-CICD-Deployment-with-Github-Actions
1. Login to AWS console.
2. Create IAM user for deployment
#with specific access

1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


#Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

#Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess
3. Create ECR repo to store/save docker image
- Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/chicken
4. Create EC2 machine (Ubuntu)
5. Open EC2 and Install docker in EC2 Machine:
#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
6. Configure EC2 as self-hosted runner:
setting>actions>runner>new self hosted runner> choose os> then run command one by one
7. Setup github secrets:
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = us-east-1

AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

ECR_REPOSITORY_NAME = simple-app