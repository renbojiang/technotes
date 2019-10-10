# Day 2
## Networking
### VPC
**Usage Pattern**
- Multi-VPC Pattern
- Multi-Account Pattern

**Limits**
- 5 VPCs per region per account
- CIDR: /24 (256) ~ /16 (65536)

**VPC Plus**
- 可追加4个网段 （比如： 10.10.0.0/16, 10.11.0.0/16）
- 通过route table  让各个CIDR互连

| destination | target |
|--|--|
| 10.10.0.0/16 | local |
| 10.11.0.0/16 | local |


**TIPS**
 - AWS里没有用broadcast，组播 
 - 用R53解决On-premise 服务器与VPC内部server的通信 default
 - 路由表不建议在生产环境中使用

**CIDR**
10.10.0.0 / 16
- .2: DNS
- 10.10.1.0/24
	- 1.0: Name
	- 1.1: Gateway
	- 1.2: DNS relay
	- 1.3: reserved

**Subnet**
- AWS reserve file IP for each subnet
- Use custom route tables for each subnet
- public subnet should meeting 4 requirements
	- VPC -> IGW
	- Public IP
	- Public Route Table (0.0.0.0/0)
	- Allow 0.0.0.0/0

**NAT Gateway （NGW）**
- NAT Gateway 是在public subnet的，具有public ip （Elastic IP）。
- NAT Gateway： outbound public internet access。
- 访问其他AWS service也会经过NGW。
- 确保每个AZ有一个NGW
- NAT instance (EC2) 已经被NAT Gateway取代。 
- 在AZ级别scale in/out
- 没有带宽限制。 AWS卖流量不卖带宽。

**Elastic Network Interface (ENI)**
- security group (安全组总是关联到ENI的)
- private IP
- elastic ip 
- mac address

> 共有子网中的Instance，建议有两张ENI与其关联。 
> 一个ENI负责业务（公网流量）
> 一个ENI负责管理 （SSH）

**Elastic IP**
- 申请但不使用要付费
- Five allowed for AWS region

**Security Group**
- Rules are stateful (进查出不查)
- Default （拒绝所有in，允许所有out，所以Inbound是白名单）
- Inbound rule 关联另一个security group可以简化配置
> 不要把Security Group的权限设置过大，最好每一种权限一个Security Group。
> 比如80，443，22各一个。
> 然后把多个security group 关联到一个多个ENI

**Access Control List (ACLs)**
- stateless (in/out 都要检查), require explicit rules for both inbound and outbound traffic
- 
<!--stackedit_data:
eyJoaXN0b3J5IjpbNTM5NTkyMTc3LDEyMzc5MTk2MTEsMTUwMz
c4NDc3NiwtMjczOTY1ODEzLC0xMDYwMjMyMzcxLDE2NjgxNjEw
NTMsODExMDM4NTk4LC0xMTc1MTc0MTQ5LC0yMTIwMjQzOTUsLT
EzMTk5MDM3NjMsNDI0MzkzNTgzLDE4Mzg1MTY3NDVdfQ==
-->