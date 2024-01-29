# Machine-Learning-Project-using-MLFlow

## For Dagshub:

MLFLOW_TRACKING_URI=https://dagshub.com/niloycste/Machine-Learning-Project-using-MLFlow.mlflow \
MLFLOW_TRACKING_USERNAME=niloycste \
MLFLOW_TRACKING_PASSWORD=55343c50b515f85d83d1bbecdf5e45f6664231d3 \
python script.py

```bash 
export MLFLOW_TRACKING_URI=https://dagshub.com/niloycste/Machine-Learning-Project-using-MLFlow.mlflow 
export MLFLOW_TRACKING_USERNAME=niloycste 
export MLFLOW_TRACKING_PASSWORD=55343c50b515f85d83d1bbecdf5e45f6664231d3 

```

## MLflow on AWS Setup:
- Login to AWS console.
- Create IAM user with AdministratorAccess
- Export the credentials in your AWS CLI by running "aws configure"
- Create a s3 bucket
- Create EC2 machine (Ubuntu) & add Security groups 5000 port

**Run the following command on EC2 machine**
```bash
sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv

sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell


## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-buc23

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI=http://ec2-54-147-36-34.compute-1.amazonaws.com:5000/


```    



