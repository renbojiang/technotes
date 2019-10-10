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
AWS里没有用broadcast，组播
用R53解决On-premise 服务器与VPC内部server的通信

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

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM3ODc1Mzc3MCwtMTE3NTE3NDE0OSwtMj
EyMDI0Mzk1LC0xMzE5OTAzNzYzLDQyNDM5MzU4MywxODM4NTE2
NzQ1XX0=
-->