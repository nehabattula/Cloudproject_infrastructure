<h1>ASSIGNMENT 4:</h1>

##  Instructions to set up infrastructure:

### 1) Set the profile to dev account and region as follows:
###    set AWS_PROFILE=dev
###    set AWS_REGION=us-east-1
### 2)  aws ec2 describe-vpcs (to display VPCs of the profile that is set above.)
### 3) Create a yml file comprising of all the Parameters provided for ec2 and attach security group to it
### 4) Create a json file to pass it parameters to the yml file for creating the stack
### 5) Run the following commands to create a stack using cloud formation in dev environment:

### a) Copy the AMI id of the one created by packer file and paste it in the "ImageAMIId" variable of parameters.json (dev)
### b) Run the following command to create the stack
###    - aws cloudformation deploy --profile dev --region us-east-1 --stack-name teststack1 --template-file csye6225-infra.yml --parameter-overrides file://parameters.json
### c) Copy the AMI id of the one created by packer file and paste it in the "ImageAMIId" variable of parameters.json (demo)
###    - aws cloudformation deploy --profile demo --region us-east-1 --stack-name teststack1 --template-file csye6225-infra.yml --parameter-overrides file://parameters.json
### d) The stack gets created and the ec2 instance will be up and running.
### e) Once the stack is created, go to the EC2 instance and copy the IPV4 of the instance and use it as an endpoint to hit the APIs using postman
### f) Reboot the instance to check if the app is still running
### g) To clean-up the resources
###    - aws cloudformation delete-stack --stack-name teststack1 --region us-east-1 --profile dev

##  Tools Used
### VSCode
