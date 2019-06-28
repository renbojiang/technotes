
# Basic Concepts

### when you should put multiple containers in the same task definition if:
-   Containers share a common lifecycle (that is, they should be launched and terminated together).
-   Containers are required to be run on the same underlying host (that is, one container references the other on a localhost port).
-   You want your containers to share resources.
-   Your containers share data volumes.

Otherwise, you should define your containers in separate tasks definitions so that you can scale, provision, and deprovision them separately.


## References
### Fargate vs. EC2
- [Di](https://cloudonaut.io/ecs-vs-fargate-whats-the-difference/)
- 

<!--stackedit_data:
eyJoaXN0b3J5IjpbNzEyMjcwODU0LDEzNTM4MTk4MTMsLTY3OT
c2MDMzMywxMDE0MDM1NDAsLTE5NTkyODIxNDMsMTI0ODk2MzYx
MywxNDUzODM0MzAyLC0yMTA5MTMxNDgxLC02OTkyNjY0OTksNz
YwNDE1OTY4LDE2NDg3NTExMTgsLTE5ODQ2NjIxNDUsMTAwMzYx
OTM0OSwxNDI3ODg5NjkxLDU0NTYxMTM3OCwxOTY1ODEzMDEsMT
g4OTQ3NDY2MywyMDQ5MDI2NjExLDEyOTkxMzAzOTYsNTg5NTk1
MTk1XX0=
-->