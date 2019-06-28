
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
- 

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTU4NDY5ODc2NiwxMzUzODE5ODEzLC02Nz
k3NjAzMzMsMTAxNDAzNTQwLC0xOTU5MjgyMTQzLDEyNDg5NjM2
MTMsMTQ1MzgzNDMwMiwtMjEwOTEzMTQ4MSwtNjk5MjY2NDk5LD
c2MDQxNTk2OCwxNjQ4NzUxMTE4LC0xOTg0NjYyMTQ1LDEwMDM2
MTkzNDksMTQyNzg4OTY5MSw1NDU2MTEzNzgsMTk2NTgxMzAxLD
E4ODk0NzQ2NjMsMjA0OTAyNjYxMSwxMjk5MTMwMzk2LDU4OTU5
NTE5NV19
-->