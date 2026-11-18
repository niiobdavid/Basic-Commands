
# ☁️ AWS CLI Commands

## 1. Basic AWS Commands

| Command | Description |
|---------|-------------|
| `aws --version` | Check AWS CLI version |
| `aws configure` | Configure AWS credentials and region |
| `aws configure list` | Show current AWS configuration |
| `aws configure list-profiles` | List configured AWS profiles |
| `aws sts get-caller-identity` | Show AWS account and authenticated identity |
| `aws help` | Display AWS CLI help |
| `aws s3 help` | Display S3 command help |

---

## 2. AWS S3 - Storage

Amazon S3 (Simple Storage Service) is used to store files, backups, images, and other objects.

| Command | Description |
|---------|-------------|
| `aws s3 ls` | List S3 buckets |
| `aws s3 ls s3://my-bucket` | List files in a bucket |
| `aws s3 mb s3://my-bucket` | Create an S3 bucket |
| `aws s3 cp file.txt s3://my-bucket/` | Upload a file to S3 |
| `aws s3 cp s3://my-bucket/file.txt .` | Download a file from S3 |
| `aws s3 sync ./folder s3://my-bucket/` | Sync a local folder to S3 |
| `aws s3 rm s3://my-bucket/file.txt` | Delete a file from S3 |
| `aws s3 rb s3://my-bucket` | Delete an empty S3 bucket |

---

## 3. AWS EC2 - Virtual Servers

Amazon EC2 (Elastic Compute Cloud) provides virtual servers in the AWS cloud.

| Command | Description |
|---------|-------------|
| `aws ec2 describe-instances` | List EC2 instances |
| `aws ec2 describe-regions` | List AWS regions |
| `aws ec2 describe-vpcs` | List Virtual Private Clouds |
| `aws ec2 describe-subnets` | List subnets |
| `aws ec2 describe-security-groups` | List security groups |
| `aws ec2 describe-volumes` | List EBS storage volumes |
| `aws ec2 describe-key-pairs` | List EC2 key pairs |
| `aws ec2 start-instances --instance-ids ID` | Start an EC2 instance |
| `aws ec2 stop-instances --instance-ids ID` | Stop an EC2 instance |
| `aws ec2 reboot-instances --instance-ids ID` | Restart an EC2 instance |

---

## 4. AWS IAM - Users and Permissions

AWS Identity and Access Management (IAM) controls access to AWS resources.

| Command | Description |
|---------|-------------|
| `aws iam list-users` | List IAM users |
| `aws iam list-groups` | List IAM groups |
| `aws iam list-roles` | List IAM roles |
| `aws iam list-policies` | List IAM policies |
| `aws iam get-user` | Get current IAM user details |
| `aws iam create-user --user-name USER` | Create an IAM user |
| `aws iam delete-user --user-name USER` | Delete an IAM user after removing dependencies |
| `aws iam list-access-keys --user-name USER` | List a user's access key metadata |

---

## 5. AWS VPC - Networking

Amazon VPC (Virtual Private Cloud) allows you to manage networking resources within AWS.

| Command | Description |
|---------|-------------|
| `aws ec2 describe-vpcs` | List VPCs |
| `aws ec2 describe-subnets` | List subnets |
| `aws ec2 describe-route-tables` | List route tables |
| `aws ec2 describe-internet-gateways` | List internet gateways |
| `aws ec2 describe-nat-gateways` | List NAT gateways |
| `aws ec2 describe-network-acls` | List network ACLs |
| `aws ec2 describe-security-groups` | List security groups |
| `aws ec2 describe-addresses` | List Elastic IP addresses |

---

## 6. AWS CloudWatch - Monitoring

Amazon CloudWatch provides monitoring, metrics, alarms, and logs for AWS resources.

| Command | Description |
|---------|-------------|
| `aws cloudwatch list-metrics` | List CloudWatch metrics |
| `aws cloudwatch describe-alarms` | List CloudWatch alarms |
| `aws logs describe-log-groups` | List log groups |
| `aws logs describe-log-streams --log-group-name NAME` | List log streams |
| `aws logs tail NAME` | Display recent logs |

---

## 7. AWS Lambda - Serverless

AWS Lambda allows you to execute code without managing servers.

| Command | Description |
|---------|-------------|
| `aws lambda list-functions` | List Lambda functions |
| `aws lambda get-function --function-name NAME` | Get Lambda function details |
| `aws lambda delete-function --function-name NAME` | Delete a Lambda function |
| `aws lambda list-layers` | List Lambda layers |

---

## 8. AWS RDS - Databases

Amazon Relational Database Service (RDS) is used to manage relational databases in AWS.

| Command | Description |
|---------|-------------|
| `aws rds describe-db-instances` | List RDS database instances |
| `aws rds describe-db-clusters` | List database clusters |
| `aws rds describe-db-snapshots` | List database snapshots |
| `aws rds describe-db-subnet-groups` | List database subnet groups |

---

## 9. AWS EKS and ECS - Containers

Amazon EKS and ECS are AWS services used for managing containerized applications.

| Command | Description |
|---------|-------------|
| `aws eks list-clusters` | List EKS Kubernetes clusters |
| `aws eks describe-cluster --name NAME` | Show EKS cluster details |
| `eksctl delete cluster --name NAME` | Delete EKS cluster |
| `aws ecs list-clusters` | List ECS clusters |
| `aws ecs list-tasks --cluster NAME` | List ECS tasks |
| `aws ecs list-services --cluster NAME` | List ECS services |
| `aws ecs stop-task --cluster NAME --task TASK-ID` | Stop any leftover tasks |
| `aws ecs delete-service --cluster my-cluster --service my-service --force` | Delete service |

---

## 10. AWS CLI Troubleshooting

Useful commands for troubleshooting AWS configuration, permissions, networking, and cloud resources.

| Command | Description |
|---------|-------------|
| `aws --version` | Verify AWS CLI installation |
| `aws configure list` | Check configured credentials and region |
| `aws sts get-caller-identity` | Verify authenticated AWS identity |
| `aws s3 ls --debug` | Debug an S3 request |
| `aws ec2 describe-instances --region eu-central-1` | Check EC2 instances in a specific region |
| `aws ec2 describe-instance-status --include-all-instances` | Check EC2 instance status |
| `aws cloudwatch describe-alarms` | Check CloudWatch alarms |
| `aws logs describe-log-groups` | Find available log groups |
## 📝 NB
- Replace `ID`, `NAME`, `USER`, and `my-bucket` with actual AWS resource values

## 11. AWS ECR - Elastic Container Registry

Amazon ECR (Elastic Container Registry) is a fully managed AWS container registry used to store, manage, and deploy Docker container images.

| Command | Description |
|---------|-------------|
| `aws ecr describe-repositories` | List ECR repositories |
| `aws ecr create-repository --repository-name my-repo` | Create an ECR repository |
| `aws ecr delete-repository --repository-name my-repo` | Delete an empty ECR repository |
| `aws ecr delete-repository --repository-name my-repo --force` | Delete an ECR repository and its images |
| `aws ecr list-images --repository-name my-repo` | List images in a repository |
| `aws ecr describe-images --repository-name my-repo` | Show image details |
| `aws ecr batch-delete-image --repository-name my-repo --image-ids imageTag=latest` | Delete an image by tag |
| `aws ecr get-login-password --region eu-central-1` | Generate a Docker authentication password |
| `aws ecr get-repository-policy --repository-name my-repo` | View repository permissions |
| `aws ecr describe-image-scan-findings --repository-name my-repo --image-id imageTag=latest` | View available image vulnerability scan results |
| `aws ecr put-lifecycle-policy --repository-name my-repo --lifecycle-policy-text file://policy.json` | Configure image lifecycle rules |
| `aws ecr get-lifecycle-policy --repository-name my-repo` | View image lifecycle rules |
| `--image-scanning-configuration scanOnPush=true \` | Scan each image for known vulnerabilities whenever it’s pushed |

---

### Docker Login to AWS ECR

```bash
aws ecr get-login-password --region eu-central-1 | docker login --username AWS --password-stdin ACCOUNT_ID.dkr.ecr.eu-central-1.amazonaws.com
```

### Build a Docker Image

```bash
docker build -t my-app .
```

### Tag the Docker Image

```bash
docker tag my-app:latest ACCOUNT_ID.dkr.ecr.eu-central-1.amazonaws.com/my-repo:latest
```

### Push the Docker Image to ECR

```bash
docker push ACCOUNT_ID.dkr.ecr.eu-central-1.amazonaws.com/my-repo:latest
```

### Pull a Docker Image from ECR

```bash
docker pull ACCOUNT_ID.dkr.ecr.eu-central-1.amazonaws.com/my-repo:latest
```

---

**Note:** Replace `ACCOUNT_ID`, `my-repo`, and `eu-central-1` with your AWS account ID, repository name, and AWS region. Docker must be installed, and your AWS identity must have the required ECR permissions.


.
## 📝 NextWork
auth credentials for keypair (win)
```bash
icacls "nextwork-keypair.pem" /reset
icacls "nextwork-keypair.pem" /grant:r "enter-your-username:R"
icacls "nextwork-keypair.pem" /inheritance:r
```
auth credentials for keypair (linux/mac):

`chmod 400 nextwork-keypair.pem`

Connect to your EC2 instance: 
`ssh -i PATH TO YOUR .PEM FILE ec2-user@YOUR PUBLIC IPV4 DNS`

Install Apache Maven into your EC2 instance:
```bash
wget https://archive.apache.org/dist/maven/maven-3/3.5.2/binaries/apache-maven-3.5.2-bin.tar.gz

sudo tar -xzf apache-maven-3.5.2-bin.tar.gz -C /opt

echo "export PATH=/opt/apache-maven-3.5.2/bin:$PATH" >> ~/.bashrc

source ~/.bashrc
```

Verify Maven:
`mvn -v`

Install Java (Amazon Correto 8) into your EC2 instance:
```bash
sudo dnf install -y java-1.8.0-amazon-corretto-devel

export JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto.x86_64

export PATH=/usr/lib/jvm/java-1.8.0-amazon-corretto.x86_64/jre/bin/:$PATH
```
Verify Java 8:
`java -version`

wget: command not found:
`sudo yum install wget -y`

Use mvn to generate a Java web app
```bash
mvn archetype:generate \
   -DgroupId=com.nextwork.app \
   -DartifactId=nextwork-web-project \
   -DarchetypeArtifactId=maven-archetype-webapp \
   -DinteractiveMode=false
```

Modify index.jsp
```bash
<html>

<body>

<h2>Hello [[YOURNAME]]!</h2>

<p>This is my NextWork web application working!</p>

</body>

</html>
```

Install Git:
```bash
sudo dnf update
sudo dnf install git -y
```

Resetting your Git credentials:
```bash
git config --global --unset credential.helper
git config --local --unset credential.helper
git remote set-url origin https://<github_username>@github.com/<github_username>/<repository_name>.git
```

Initiate Git:
`git init`

Connect local project folder with Github repo:
`git remote add origin enter your github repo link`

Git Add, Commit, Push
```bash
git add . 

git commit -m "Updated index.jsp with new content"

git push -u origin master

```
History of commits:
`git log`

Changes staged:
`git diff --staged`

codeartifact-nextwork-consumer-policy: 
```bash
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "codeartifact:GetAuthorizationToken",
                "codeartifact:GetRepositoryEndpoint",
                "codeartifact:ReadFromRepository"
            ],
            "Resource": "*"
        },
        {
            "Effect": "Allow",
            "Action": "sts:GetServiceBearerToken",
            "Resource": "*",
            "Condition": {
                "StringEquals": {
                    "sts:AWSServiceName": "codeartifact.amazonaws.com"
                }
            }
        }
    ]
}
```
settings.xml:
```bash
<settings>
</settings>
```
compile project
```bash
mvn -s settings.xml compile
```
echo "Hellooooo this is a test package!" > secret-mission.txt
bundle the file into a package:
```bash
tar -czvf secret-mission.tar.gz secret-mission.txt
```
Generate Security Hash:
```bash
export ASSET_SHA256=$(sha256sum secret-mission.tar.gz | awk '{print $1;}')
```
Confirm hash generation:
`echo $ASSET_SHA256`

Deploy Your Secret Package:
```bash
aws codeartifact publish-package-version \
  --domain nextwork \
  --repository nextwork-devops-cicd \
  --format generic \
  --namespace secret-mission \
  --package secret-mission \
  --package-version 1.0.0 \
  --asset-content secret-mission.tar.gz \
  --asset-name secret-mission.tar.gz \
  --asset-sha256 $ASSET_SHA256
```

# Deploying Kubernetes
download, extract, and install eksctl:
```bash
curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
sudo mv -v /tmp/eksctl /usr/local/bin
```

Verify: 
`eksctl version`

Create an eks cluster:
```bash
eksctl create cluster \
  --name nextwork-eks-cluster \
  --nodegroup-name nextwork-nodegroup \
  --node-type t3.micro \
  --nodes 3 \
  --nodes-min 1 \
  --nodes-max 3 \
  --version 1.33 \
  --region your-region-code
```
Install Git:
```bash
sudo dnf update
sudo dnf install git -y
```

Verify Git Version:
`git --version`

Configure Git:
```bash
git config --global user.name "yourname"
git config --global user.email "email"
```
Clone Git:
`git clone your-github-url`

Install Docker:
`sudo yum install -y docker`

Start Docker:
`sudo service docker start`

Add ec2-user to the Docker group:
`sudo usermod -a -G docker ec2-user`

Make sure your ec2-user has been added to the Docker group:
`groups ec2-user`

Build a container image:
`docker build -t your-backend-image-folder .`

Create a new Amazon ECR repository:
```bash
aws ecr create-repository \
  --repository-name nextwork-flask-backend \
  --image-scanning-configuration scanOnPush=true
```
Create Deployment manifest file:
```bash
cat << EOF > flask-deployment.yaml
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nextwork-flask-backend
  namespace: default
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nextwork-flask-backend
  template:
    metadata:
      labels:
        app: nextwork-flask-backend
    spec:
      containers:
        - name: nextwork-flask-backend
          image: your-ecr-image-url
          ports:
            - containerPort: 8080
EOF
```
Create Service manifest file:
```bash
cat << EOF > flask-service.yaml
---
apiVersion: v1
kind: Service
metadata:
  name: nextwork-flask-backend
spec:
  selector:
    app: nextwork-flask-backend
  type: NodePort
  ports:
    - port: 8080
      targetPort: 8080
      protocol: TCP
EOF
```
Install kubectl:
```bash
sudo curl -o /usr/local/bin/kubectl \
https://s3.us-west-2.amazonaws.com/amazon-eks/1.31.0/2024-09-12/bin/linux/amd64/kubectl
```
Grant permission:
```bash
sudo chmod +x /usr/local/bin/kubectl
```
Apply the manifests:
```bash
kubectl apply -f flask-deployment.yaml
kubectl apply -f flask-service.yaml
```
If error in Applying:
```bash
aws eks update-kubeconfig --name cluster-name --region your-region-code
```
Set up access to cluster nodes:
```bash
eksctl create iamidentitymapping --cluster nextwork-eks-cluster --arn your-user-arn --group system:masters --username admin --region your-region-code
```
# Terraform
Registry's documentation on S3:
https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket

Initalize Terraform:
`terraform init`

Plan Terraform configuration:
`terraform plan`

Apply Terraform Configuration:
`terraform apply`

Downloading AWS CLI (win):
```bash
Invoke-WebRequest -Uri "https://awscli.amazonaws.com/AWSCLIV2.msi" -OutFile "AWSCLIV2.msi"
Start-Process msiexec.exe -ArgumentList "/i AWSCLIV2.msi" -Wait
```

Configure the AWS CLI:
`aws configure`

Delete Resources with Terraform:
`terraform destroy`
