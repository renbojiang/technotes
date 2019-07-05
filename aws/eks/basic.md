
[https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html](https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html)

[https://docs.aws.amazon.com/eks/latest/userguide/install-aws-iam-authenticator.html](https://docs.aws.amazon.com/eks/latest/userguide/install-aws-iam-authenticator.html)

[https://docs.aws.amazon.com/eks/latest/userguide/troubleshooting.html#unauthorized](https://docs.aws.amazon.com/eks/latest/userguide/troubleshooting.html#unauthorized)

[https://docs.aws.amazon.com/eks/latest/userguide/add-user-role.html](https://docs.aws.amazon.com/eks/latest/userguide/add-user-role.html)

[https://www.youtube.com/watch?v=6H5sXQoJiso](https://www.youtube.com/watch?v=6H5sXQoJiso)

[https://github.com/Kurento/Kubernetes/blob/master/nginx-deployment-service.yaml](https://github.com/Kurento/Kubernetes/blob/master/nginx-deployment-service.yaml)

[https://eksworkshop.com/introduction/eks/eks_high_level/](https://eksworkshop.com/introduction/eks/eks_high_level/)


```
aws eks update-kubeconfig --name acadci --region us-west-2
```


[https://docs.aws.amazon.com/eks/latest/userguide/dashboard-tutorial.html](https://docs.aws.amazon.com/eks/latest/userguide/dashboard-tutorial.html)

eksctl & kubectl installation
 - [kubectl](https://eksworkshop.com/prerequisites/k8stools/)
 - [eksctl](https://eksctl.io/introduction/installation/)
configure our aws cli with our current region as default:
```
export ACCOUNT_ID=$(aws sts get-caller-identity --output text --query Account) 
export AWS_REGION=$(curl -s 169.254.169.254/latest/dynamic/instance-identity/document | jq -r '.region') 
echo  "export ACCOUNT_ID=${ACCOUNT_ID}" >> ~/.bash_profile 
echo  "export AWS_REGION=${AWS_REGION}" >> ~/.bash_profile 
aws configure set default.region ${AWS_REGION} 
aws configure get default.region
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzMxMTA1NzUsLTE2NzgwNDI3MjMsMTkyOT
E5NjcxMCwtMTAyNTk1NTcxMSwyMDk5MzA3MDE1LDU2OTI0MDUz
MiwtMTMyODc2MDk3NSwtMjA3MjAyMjI2Ml19
-->