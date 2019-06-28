
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


[https://www.youtube.com/watch?v=fMGd9IUaotE](https://www.youtube.com/watch?v=fMGd9IUaotE)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY1MzE1NDIwNywxMzE2MDc5MDU2LDExNT
Y5MDUwNjEsLTEzNDM4ODgzMjcsMTM1MzgxOTgxMywtNjc5NzYw
MzMzLDEwMTQwMzU0MCwtMTk1OTI4MjE0MywxMjQ4OTYzNjEzLD
E0NTM4MzQzMDIsLTIxMDkxMzE0ODEsLTY5OTI2NjQ5OSw3NjA0
MTU5NjgsMTY0ODc1MTExOCwtMTk4NDY2MjE0NSwxMDAzNjE5Mz
Q5LDE0Mjc4ODk2OTEsNTQ1NjExMzc4LDE5NjU4MTMwMSwxODg5
NDc0NjYzXX0=
-->