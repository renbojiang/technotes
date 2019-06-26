
# Basic Concepts

## VPC Networking Components
### [Elastic Network Interfaces](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html)
Description
>An elastic network interface (referred to as a  _network interface_  in this documentation) is a logical networking component in a VPC that represents a virtual network card.

### [Route Tables](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html)
Description
>A  _route table_  contains a set of rules, called  _routes_, that are used to determine where network traffic is directed.
>Each subnet in your VPC must be associated with a route table; the table controls the routing for the subnet. A subnet can only be associated with one route table at a time, but you can associate multiple subnets with the same route table.

One way to protect your VPC is to leave the main route table in its original default state (with only the local route), and explicitly associate each new subnet you create with one of the custom route tables you've created.



### [DHCP Options](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_DHCP_Options.html)
Description
>The Dynamic Host Configuration Protocol (DHCP) provides a standard for passing configuration information to hosts on a TCP/IP network. The `options` field of a DHCP message contains the configuration parameters. Some of those parameters are the domain name, domain name server, and the netbios-node-type.

Amazon DNS Server
>When you create a VPC, we automatically create a set of DHCP options and associate them with the VPC. This set includes two options:  `domain-name-servers=AmazonProvidedDNS`, and  `domain-name=`_`domain-name-for-your-region`_. AmazonProvidedDNS is an Amazon DNS server, and this option enables DNS for instances that need to communicate over the VPC's Internet gateway. The string  `AmazonProvidedDNS`  maps to a DNS server running on a reserved IP address at the base of the VPC IPv4 network range, plus two. For example, the DNS Server on a 10.0.0.0/16 network is located at 10.0.0.2. For VPCs with multiple IPv4 CIDR blocks, the DNS server IP address is located in the primary CIDR block.
>
>When you launch an instance into a VPC, we provide the instance with a private DNS hostname, and a public DNS hostname if the instance receives a public IPv4 address. If  `domain-name-servers`  in your DHCP options is set to AmazonProvidedDNS, the public DNS hostname takes the form  ``ec2-_`public-ipv4-address`_.compute-1.amazonaws.com``  for the us-east-1 region, and  ``ec2-_`public-ipv4-address`_._`region`_.compute.amazonaws.com``  for other regions. The private hostname takes the form  ``ip-_`private-ipv4-address`_.ec2.internal``  for the us-east-1 region, and  ``ip-_`private-ipv4-address`_._`region`_.compute.internal``  for other regions. To change these to custom DNS hostnames, you must set  `domain-name-servers`  to a custom DNS server.

### [Route Tables](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html)
Description
>A  _route table_  contains a set of rules, called  _routes_, that are used to determine where network traffic is directed.
>Each subnet in your VPC must be associated with a route table; the table controls the routing for the subnet. A subnet can only be associated with one route table at a time, but you can associate multiple subnets with the same route table.

### [NAT Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html)
Description
> NAT: Network Address Translation. You can use a NAT device to enable instances in a private subnet to connect to the internet, but prevent the internet from initiating connections with the instances.When traffic goes to the internet, the source IPv4 address is replaced with the NAT device’s address and similarly, when the response traffic goes to those instances, the NAT device translates the address back to those instances’ private IPv4 addresses.
>NAT devices are not supported for IPv6 traffic—use an egress-only Internet gateway instead

The actual role of a NAT device is both address translation and port address translation (PAT).

Two kinds of NAT devices—a _NAT gateway_ or a _NAT instance_. We recommend NAT gateways, as they provide better availability and bandwidth over NAT instances.


### [Security Groups](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html)
Description
>A _security group_ acts as a virtual firewall for your instance to control inbound and outbound traffic. When you launch an instance in a VPC, you can assign up to five security groups to the instance. Security groups act at the instance level, not the subnet level.



### [Internet Gateways](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html)

**Definition**: 
>An internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet. It therefore imposes no availability risks or bandwidth constraints on your network traffic.

**Purposes**: 
- to provide a target in your VPC route tables for internet-routable traffic
- to perform network address translation (NAT) for instances that have been assigned public IPv4 addresses.

**Enabling Internet Access**  
To enable access to or from the internet for instances in a VPC subnet, you must do the following:
-   Attach an internet gateway to your VPC.
-   Ensure that your subnet's route table points to the internet gateway.
-   Ensure that instances in your subnet have a globally unique IP address (public IPv4 address, Elastic IP address, or IPv6 address).
-   Ensure that your network access control and security group rules allow the relevant traffic to flow to and from your instance.


AWS Help Doc: 
[https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html)



- 3 stacks running on Fargate
- DNS naming binding (acadci.autodesk.com)
- persistent disk volume 
- 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0OTY5OTEzMzcsMTAxNDAzNTQwLC0xOT
U5MjgyMTQzLDEyNDg5NjM2MTMsMTQ1MzgzNDMwMiwtMjEwOTEz
MTQ4MSwtNjk5MjY2NDk5LDc2MDQxNTk2OCwxNjQ4NzUxMTE4LC
0xOTg0NjYyMTQ1LDEwMDM2MTkzNDksMTQyNzg4OTY5MSw1NDU2
MTEzNzgsMTk2NTgxMzAxLDE4ODk0NzQ2NjMsMjA0OTAyNjYxMS
wxMjk5MTMwMzk2LDU4OTU5NTE5NV19
-->