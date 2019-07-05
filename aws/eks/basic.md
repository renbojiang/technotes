
[https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html](https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html)

[https://docs.aws.amazon.com/eks/latest/userguide/install-aws-iam-authenticator.html](https://docs.aws.amazon.com/eks/latest/userguide/install-aws-iam-authenticator.html)

[https://docs.aws.amazon.com/eks/latest/userguide/troubleshooting.html#unauthorized](https://docs.aws.amazon.com/eks/latest/userguide/troubleshooting.html#unauthorized)

[https://docs.aws.amazon.com/eks/latest/userguide/add-user-role.html](https://docs.aws.amazon.com/eks/latest/userguide/add-user-role.html)

[https://www.youtube.com/watch?v=6H5sXQoJiso](https://www.youtube.com/watch?v=6H5sXQoJiso)

[https://github.com/Kurento/Kubernetes/blob/master/nginx-deployment-service.yaml](https://github.com/Kurento/Kubernetes/blob/master/nginx-deployment-service.yaml)

[https://eksworkshop.com/introduction/eks/eks_high_level/](https://eksworkshop.com/introduction/eks/eks_high_level/)





[https://docs.aws.amazon.com/eks/latest/userguide/dashboard-tutorial.html](https://docs.aws.amazon.com/eks/latest/userguide/dashboard-tutorial.html)

eksctl & kubectl installation
 - [kubectl](https://eksworkshop.com/prerequisites/k8stools/)
 - [eksctl](https://eksctl.io/introduction/installation/)
 - [helm](https://eksworkshop.com/helm_root/helm_intro/install/)
 - [aws-iam-authenticator](https://docs.aws.amazon.com/eks/latest/userguide/install-aws-iam-authenticator.html)

configure our aws cli with our current region as default:
```
export ACCOUNT_ID=$(aws sts get-caller-identity --output text --query Account) 
export AWS_REGION=$(curl -s 169.254.169.254/latest/dynamic/instance-identity/document | jq -r '.region') 
echo  "export ACCOUNT_ID=${ACCOUNT_ID}" >> ~/.bash_profile 
echo  "export AWS_REGION=${AWS_REGION}" >> ~/.bash_profile 
aws configure set default.region ${AWS_REGION} 
aws configure get default.region
```
update kubeconfig
```
aws eks update-kubeconfig --name acadci --region us-west-2
```

helm install
```bash
helm install nginx --tiller-namespace tiller-world --namespace tiller-world
```

```
helm install --name websvr bitnami/nginx --set service.annotations."service\.beta\.kubernetes\.io/load-balancer-source-ranges"="10.0.0.0/8" --set service.annotations."service\.beta\.kubernetes\.io/aws-load-balancer-internal"="0.0.0.0/0" --namespace staging
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc4ODg5MjcyNSwxNTI5MTEyMzE5LC04MT
Y5MTg1MTUsNjEyNTcwNTc4LDE4MDg4NDM2NTQsMTM1ODAyMjA1
NCwzMzExMDU3NSwtMTY3ODA0MjcyMywxOTI5MTk2NzEwLC0xMD
I1OTU1NzExLDIwOTkzMDcwMTUsNTY5MjQwNTMyLC0xMzI4NzYw
OTc1LC0yMDcyMDIyMjYyXX0=
-->