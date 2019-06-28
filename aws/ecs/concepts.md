
# Basic Concepts

### when you should put multiple containers in the same task definition if:
-   Containers share a common lifecycle (that is, they should be launched and terminated together).
-   Containers are required to be run on the same underlying host (that is, one container references the other on a localhost port).
-   You want your containers to share resources.
-   Your containers share data volumes.

Otherwise, you should define your containers in separate tasks definitions so that you can scale, provision, and deprovision them separately.


## References
[AWS ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html)

### Fargate vs. EC2
- [Difference](https://cloudonaut.io/ecs-vs-fargate-whats-the-difference/)
- [Pricing](https://containersonaws.com/introduction/ec2-or-aws-fargate/)
- [https://www.janbasktraining.com/blog/what-is-aws-fargate/](https://www.janbasktraining.com/blog/what-is-aws-fargate/)

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE1NjkwNTA2MSwtMTM0Mzg4ODMyNywxMz
UzODE5ODEzLC02Nzk3NjAzMzMsMTAxNDAzNTQwLC0xOTU5Mjgy
MTQzLDEyNDg5NjM2MTMsMTQ1MzgzNDMwMiwtMjEwOTEzMTQ4MS
wtNjk5MjY2NDk5LDc2MDQxNTk2OCwxNjQ4NzUxMTE4LC0xOTg0
NjYyMTQ1LDEwMDM2MTkzNDksMTQyNzg4OTY5MSw1NDU2MTEzNz
gsMTk2NTgxMzAxLDE4ODk0NzQ2NjMsMjA0OTAyNjYxMSwxMjk5
MTMwMzk2XX0=
-->