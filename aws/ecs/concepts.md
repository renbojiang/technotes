
# Basic Concepts

## VPC Networking Components
### [Elastic Network Interfaces](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html)
Description
>An elastic network interface (referred to as a  _network interface_  in this documentation) is a logical networking component in a VPC that represents a virtual network card.

### [DHCP Options](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_DHCP_Options.html)
Description
>The Dynamic Host Configuration Protocol (DHCP) provides a standard for passing configuration information to hosts on a TCP/IP network. The `options` field of a DHCP message contains the configuration parameters. Some of those parameters are the domain name, domain name server, and the netbios-node-type.

Amazon DNS Server
>When you create a VPC, we automatically create a set of DHCP options and associate them with the VPC. This set includes two options:  `domain-name-servers=AmazonProvidedDNS`, and  `domain-name=`_`domain-name-for-your-region`_. AmazonProvidedDNS is an Amazon DNS server, and this option enables DNS for instances that need to communicate over the VPC's Internet gateway. The string  `AmazonProvidedDNS`  maps to a DNS server running on a reserved IP address at the base of the VPC IPv4 network range, plus two. For example, the DNS Server on a 10.0.0.0/16 network is located at 10.0.0.2. For VPCs with multiple IPv4 CIDR blocks, the DNS server IP address is located in the primary CIDR block.

When you launch an instance into a VPC, we provide the instance with a private DNS hostname, and a public DNS hostname if the instance receives a public IPv4 address. If  `domain-name-servers`  in your DHCP options is set to AmazonProvidedDNS, the public DNS hostname takes the form  ``ec2-_`public-ipv4-address`_.compute-1.amazonaws.com``  for the us-east-1 region, and  ``ec2-_`public-ipv4-address`_._`region`_.compute.amazonaws.com``  for other regions. The private hostname takes the form  ``ip-_`private-ipv4-address`_.ec2.internal``  for the us-east-1 region, and  ``ip-_`private-ipv4-address`_._`region`_.compute.internal``  for other regions. To change these to custom DNS hostnames, you must set  `domain-name-servers`  to a custom DNS server.

The Amazon DNS server in your VPC is used to resolve the DNS domain names that you specify in a private hosted zone in Route 53. For more information about private hosted zones, see  [Working with Private Hosted Zones](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/hosted-zones-private.html)  in the  _Amazon Route 53 Developer Guide_.

Services that use the Hadoop framework, such as Amazon EMR, require instances to resolve their own fully qualified domain names (FQDN). In such cases, DNS resolution can fail if the  `domain-name-servers`  option is set to a custom value. To ensure proper DNS resolution, consider adding a conditional forwarder on your DNS server to forward queries for the domain  ``_`region-name`_.compute.internal``  to the Amazon DNS server. For more information, see  [Setting Up a VPC to Host Clusters](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-vpc-host-job-flows.html)  in the  _Amazon EMR Management Guide_.

Note

You can use the Amazon DNS server IP address 169.254.169.253, though some servers don't allow its use. Windows Server 2008, for example, disallows the use of a DNS server located in the 169.254.x.x network range.


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
eyJoaXN0b3J5IjpbMjA0MDk3OTAxMiwxMDAzNjE5MzQ5LDE0Mj
c4ODk2OTEsNTQ1NjExMzc4LDE5NjU4MTMwMSwxODg5NDc0NjYz
LDIwNDkwMjY2MTEsMTI5OTEzMDM5Niw1ODk1OTUxOTVdfQ==
-->