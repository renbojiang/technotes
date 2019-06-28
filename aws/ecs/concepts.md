
# Basic Concepts

### when you should put multiple containers in the same task definition if:
-   Containers share a common lifecycle (that is, they should be launched and terminated together).
-   Containers are required to be run on the same underlying host (that is, one container references the other on a localhost port).
-   You want your containers to share resources.
-   Your containers share data volumes.

Otherwise, you should define your containers in separate tasks definitions so that you can scale, provision, and deprovision them separately.

# Amazon ECS Deployment Types

An Amazon ECS deployment type determines the deployment strategy that your service uses. There are three deployment types: rolling update, blue/green, and external.

**Topics**

-   [Rolling Update](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/deployment-type-ecs.html)
-   [Blue/Green Deployment with CodeDeploy](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/deployment-type-bluegreen.html)
-   [External Deployment](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/deployment-type-external.html)


## References
[AWS ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html)

### Fargate vs. EC2
- [Difference](https://cloudonaut.io/ecs-vs-fargate-whats-the-difference/)
- [Pricing](https://containersonaws.com/introduction/ec2-or-aws-fargate/)
- [https://www.janbasktraining.com/blog/what-is-aws-fargate/](https://www.janbasktraining.com/blog/what-is-aws-fargate/)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTMxNjA3OTA1NiwxMTU2OTA1MDYxLC0xMz
QzODg4MzI3LDEzNTM4MTk4MTMsLTY3OTc2MDMzMywxMDE0MDM1
NDAsLTE5NTkyODIxNDMsMTI0ODk2MzYxMywxNDUzODM0MzAyLC
0yMTA5MTMxNDgxLC02OTkyNjY0OTksNzYwNDE1OTY4LDE2NDg3
NTExMTgsLTE5ODQ2NjIxNDUsMTAwMzYxOTM0OSwxNDI3ODg5Nj
kxLDU0NTYxMTM3OCwxOTY1ODEzMDEsMTg4OTQ3NDY2MywyMDQ5
MDI2NjExXX0=
-->