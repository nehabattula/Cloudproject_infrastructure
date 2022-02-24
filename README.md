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

### 1) To create stack by passing parameters.json file
###    - aws cloudformation deploy --profile demo --region us-east-1 --stack-name teststack1 --template-file csye6225-infra.yml --parameter-overrides file://parameters.json
### 2) Change the VpcCIDR value in the parameters.json file and the EnvironmentName and create another stack in the same region (us-east-1)
###    - aws cloudformation deploy --profile demo --region us-east-1 --stack-name teststack2 --template-file csye6225-infra.yml --parameter-overrides file://parameters.json
### 3) To create in another region, change the values for region
###    - aws cloudformation deploy --profile demo --region us-east-2 --stack-name teststack1 --template-file csye6225-infra.yml --parameter-overrides file://parameters.json
### 4) Change the VpcCIDR value in the parameters.json file and the EnvironmentName and create another stack in the same region (us-east-2)
###    - aws cloudformation deploy --profile demo --region us-east-2 --stack-name teststack2 --template-file csye6225-infra.yml --parameter-overrides file://parameters.json
### 5) To clean-up the resources
###    - aws cloudformation delete-stack --stack-name teststack1 --region us-east-1 --profile demo
###    - aws cloudformation delete-stack --stack-name teststack2 --region us-east-1 --profile demo
###    - aws cloudformation delete-stack --stack-name teststack1 --region us-east-2 --profile demo
###    - aws cloudformation delete-stack --stack-name teststack2 --region us-east-2 --profile demo

##  Tools Used
### VSCode