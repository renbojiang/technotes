
# Basic Concepts

## VPC Networking Components
### [Elastic Network Interfaces](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html)
Description
>An elastic network interface (referred to as a  _network interface_  in this documentation) is a logical networking component in a VPC that represents a virtual network card.

### [DHCP Options](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_DHCP_Options.html)
Description
>The Dynamic Host Configuration Protocol (DHCP) provides a standard for passing configuration information to hosts on a TCP/IP network. The `options` field of a DHCP message contains the configuration parameters. Some of those parameters are the domain name, domain name server, and the netbios-node-type.
>

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
eyJoaXN0b3J5IjpbMTI4MTUwMzIzMiwxMDAzNjE5MzQ5LDE0Mj
c4ODk2OTEsNTQ1NjExMzc4LDE5NjU4MTMwMSwxODg5NDc0NjYz
LDIwNDkwMjY2MTEsMTI5OTEzMDM5Niw1ODk1OTUxOTVdfQ==
-->