
# Basic Concepts

### when you should put multiple containers in the same task definition if:
-   Containers share a common lifecycle (that is, they should be launched and terminated together).
-   Containers are required to be run on the same underlying host (that is, one container references the other on a localhost port).
-   You want your containers to share resources.
-   Your containers share data volumes.

Otherwise, you should define your containers in separate tasks definitions so that you can scale, provision, and deprovision them separately.


## References
### Fargate vs. EC2
- [Difference](https://cloudonaut.io/ecs-vs-fargate-whats-the-difference/)
- [Pricing](https://containersonaws.com/introduction/ec2-or-aws-fargate/)
- [https://www.janbasktraining.com/blog/what-is-aws-fargate/](https://www.janbasktraining.com/blog/what-is-aws-fargate/)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzNDM4ODgzMjcsMTM1MzgxOTgxMywtNj
c5NzYwMzMzLDEwMTQwMzU0MCwtMTk1OTI4MjE0MywxMjQ4OTYz
NjEzLDE0NTM4MzQzMDIsLTIxMDkxMzE0ODEsLTY5OTI2NjQ5OS
w3NjA0MTU5NjgsMTY0ODc1MTExOCwtMTk4NDY2MjE0NSwxMDAz
NjE5MzQ5LDE0Mjc4ODk2OTEsNTQ1NjExMzc4LDE5NjU4MTMwMS
wxODg5NDc0NjYzLDIwNDkwMjY2MTEsMTI5OTEzMDM5Niw1ODk1
OTUxOTVdfQ==
-->