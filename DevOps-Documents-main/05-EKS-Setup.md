## Step - 1 : Create EKS Management Host in AWS ##


1. Launch EC2
--------------------------------------------------
AMI: Ubuntu
Instance: t2.micro
Purpose: EKS Management Host

Connect:
ssh -i "hk-eks.pem" ubuntu@<PUBLIC-IP>


2. Install AWS CLI
--------------------------------------------------

sudo apt update
sudo apt install -y unzip curl

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" \
-o "awscliv2.zip"

unzip awscliv2.zip

sudo ./aws/install

aws --version

Verify AWS identity:
aws sts get-caller-identity


3. Install kubectl
--------------------------------------------------

# Choose the kubectl version compatible with
# the EKS cluster Kubernetes version.

curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/<VERSION>/<DATE>/bin/linux/amd64/kubectl

chmod +x kubectl

sudo mv kubectl /usr/local/bin/

kubectl version --client


4. Install eksctl
--------------------------------------------------

ARCH=amd64
PLATFORM=$(uname -s)_$ARCH

curl -sLO \
"https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$PLATFORM.tar.gz"

tar -xzf eksctl_$PLATFORM.tar.gz -C /tmp

sudo install -m 0755 /tmp/eksctl /usr/local/bin/eksctl

eksctl version
```
## Step - 2 : Create IAM role & attach to EKS Management Host ##

1) Create New Role using IAM service ( Select Usecase - ec2 ) 	
2) Add below permissions for the role <br/>
	- Administrator - acces <br/>
		
3) Enter Role Name (eksroleec2) 
4) Attach created role to EKS Management Host (Select EC2 => Click on Security => Modify IAM Role => attach IAM role we have created) 

## Step - 3 : Create EKS Cluster using eksctl ## 
**Syntax:** 

eksctl create cluster --name cluster-name  \
--region region-name \
--node-type instance-type \
--nodes-min 2 \
--nodes-max 2 \ 
--zones <AZ-1>,<AZ-2>

## N. Virgina: <br/>
```
eksctl create cluster --name hk-cluster4 --region us-east-1 --node-type t2.medium  --zones us-east-1a,us-east-1b
```
## Mumbai: <br/>
```
eksctl create cluster --name hk-cluster4 --region ap-south-1 --node-type t2.medium  --zones ap-south-1a,ap-south-1b
```

## Note: Cluster creation will take 5 to 10 mins of time (we have to wait). After cluster created we can check nodes using below command.

```
 kubectl get nodes  
```

### Note: We should be able to see EKS cluster nodes here. ##

### We are done with our Setup ###
	
## Step - 4 : After your practise, delete Cluster and other resources we have used in AWS Cloud to avoid billing ##

```
eksctl delete cluster --name hk-cluster4 --region ap-south-1
```
