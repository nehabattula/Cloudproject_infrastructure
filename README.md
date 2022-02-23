<h1>ASSIGNMENT 3:</h1>

##  Instructions to set up infrastructure:
### Install aws cli MSI installer for windows
### Run aws --version to check the version of the aws cli that was installed
### Set the profile for dev account and demo account as follows:
### aws configure --profile=dev and then enter the access key ID, secret access key, and region- us-east-1 
### aws configure --profile=demo (for production) and then enter the access key ID, secret access key, and region: us-east-1 
### set AWS_PROFILE=dev
### set AWS_REGION=us-east-1
### aws ec2 describe-vpcs (to display VPCs of the profile that is set above.)
### Create a yml file comprising of all the Parameters, Resources
### Create a json file to pass it parameters to the yml file for creating the stack
### Run the following commands to create a stack using cloud formation:

### 1) To create a stack with name as 'teststack'
### aws cloudformation deploy --profile dev --stack-name teststack --template-file .\csye6225-infra.yml

### 2) To create stack by passing parameters.json file
### aws cloudformation deploy --profile dev --stack-name teststack --template-file csye6225-infra.yml --parameter-overrides file://parameters.json

### 3) To delete the stack named 'teststack'
### aws cloudformation delete-stack --stack-name teststack

##  Tools Used
### VSCode


