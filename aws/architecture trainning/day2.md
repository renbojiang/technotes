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

ENI
- security group
- private/public IP
- ela

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg1ODI0MTc4NCwtMjczOTY1ODEzLC0xMD
YwMjMyMzcxLDE2NjgxNjEwNTMsODExMDM4NTk4LC0xMTc1MTc0
MTQ5LC0yMTIwMjQzOTUsLTEzMTk5MDM3NjMsNDI0MzkzNTgzLD
E4Mzg1MTY3NDVdfQ==
-->