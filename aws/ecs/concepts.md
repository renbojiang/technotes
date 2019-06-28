
# Basic Concepts

> You should put multiple containers in the same task definition if:
> -   Containers share a common lifecycle (that is, they should be launched and terminated together).
> -   Containers are required to be run on the same underlying host (that is, one container references the other on a localhost port).
> -   You want your containers to share resources.
> -   Your containers share data volumes. 
> Otherwise, you should define your containers in separate tasks definitions so that you can scale, provision, and deprovision them separately.



<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg4NjkwNjE3NCwtNjc5NzYwMzMzLDEwMT
QwMzU0MCwtMTk1OTI4MjE0MywxMjQ4OTYzNjEzLDE0NTM4MzQz
MDIsLTIxMDkxMzE0ODEsLTY5OTI2NjQ5OSw3NjA0MTU5NjgsMT
Y0ODc1MTExOCwtMTk4NDY2MjE0NSwxMDAzNjE5MzQ5LDE0Mjc4
ODk2OTEsNTQ1NjExMzc4LDE5NjU4MTMwMSwxODg5NDc0NjYzLD
IwNDkwMjY2MTEsMTI5OTEzMDM5Niw1ODk1OTUxOTVdfQ==
-->