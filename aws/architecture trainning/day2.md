# Day 2
## Networking Part 1
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
 - EC2 DNS 设置用user data 实现

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
- 默认设置： allow 所有in/out bound

## Networking Part 2
**Virtual Private Gateway (VGW)**
- establish private connection between AWS VPC and another network
- On-premise DC <-> DX location <-> VGW
- 每个svi对应一个vgw吗？

**VPC Peer**
- connect VPCs
- transitive peering are NOT supported
- 可以实现cross region的efs 共享文件挂载

**Resource Access Manager**
- Share Transition Gateway
- DNS resolve rules
- Subnet
- Reserved Capacity
- 许可证配置
- ...

**Reserved Instance VS. Reserved Capacity**
- RI只是购买方式
- 真正预留资源是RC

**Endpoint Interface**
- 至于dynamo db和s3是endpoint Gateway，其他都是interface
- 可以应用security group
- 会和ENI link起来
- 建立endpoint interface 后，可以直接通过local 路由来访问对应的服务。

## Load Balancing
|| CLB | ALB| NLB
|--|--|--|--|
|health check  | ping | listener |
|backend | EC2 | target group |
|源地址|开启proxy protocol|后端更容易拿到源IP信息
|ssl offload| https external, http internal，证书轮转 | ACM
|security | |内嵌WAF |
|应用分发 | |注册的应用 | static 目标ip |

相同层面不要有异构
流量从ELB进，从NGW回

## Route 53
Cloud DNS service (100% availability)
R53 support DNS health check
可以实现基于权重的路由，比如灰度发布

CloudWatch 用于监控resource
CloudTrail 用于监控API call
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0MDQwNDMxMTQsLTE4MTk1MDY4MTMsMT
Q1NzQ0MTQyOSwtMTEzODcyMTA2NSwtMzE5ODA2MzgzLDE1MTE2
MjIyMjMsLTEyNTA1OTkzNjIsLTE1NDU1NjgxMTUsMTU0OTQzNT
czMSwtMTMyNTgzNTcwOSwtMTc3NDkzMjMyOCwxMjY4NTk3NzU4
LC0xMTA4NTEwOTksODgwMjEyNTIxLDQwNTA2MDQxMiwtMjkyND
E2OTE2LC03ODg1MjkxOSwxNjAxMzU5MjA4LDUzOTU5MjE3Nywx
MjM3OTE5NjExXX0=
-->