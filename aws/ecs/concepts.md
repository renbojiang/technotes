
# Basic Concepts

## VPC Networking Components
### [Elastic Network Interfaces](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html)
Description
>An elastic network interface (referred to as a  _network interface_  in this documentation) is a logical networking component in a VPC that represents a virtual network card.

### [Security Groups](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html)
Description
>A _security group_ acts as a virtual firewall for your instance to control inbound and outbound traffic. When you launch an instance in a VPC, you can assign up to five security groups to the instance. Security groups act at the instance level, not the subnet level.



### [Internet Gateways](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html)

**Definition**: 
An internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet. It therefore imposes no availability risks or bandwidth constraints on your network traffic.

**Purposes**: 
- to provide a target in your VPC route tables for internet-routable traffic
- to perform network address translation (NAT) for instances that have been assigned public IPv4 addresses.




AWS Help Doc: 
[https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html)


<!--stackedit_data:
eyJoaXN0b3J5IjpbMTAwMzYxOTM0OSwxNDI3ODg5NjkxLDU0NT
YxMTM3OCwxOTY1ODEzMDEsMTg4OTQ3NDY2MywyMDQ5MDI2NjEx
LDEyOTkxMzAzOTYsNTg5NTk1MTk1XX0=
-->