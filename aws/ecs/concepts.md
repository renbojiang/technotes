
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
eyJoaXN0b3J5IjpbLTE2MzYzNTk5NDgsMTE1NjkwNTA2MSwtMT
M0Mzg4ODMyNywxMzUzODE5ODEzLC02Nzk3NjAzMzMsMTAxNDAz
NTQwLC0xOTU5MjgyMTQzLDEyNDg5NjM2MTMsMTQ1MzgzNDMwMi
wtMjEwOTEzMTQ4MSwtNjk5MjY2NDk5LDc2MDQxNTk2OCwxNjQ4
NzUxMTE4LC0xOTg0NjYyMTQ1LDEwMDM2MTkzNDksMTQyNzg4OT
Y5MSw1NDU2MTEzNzgsMTk2NTgxMzAxLDE4ODk0NzQ2NjMsMjA0
OTAyNjYxMV19
-->