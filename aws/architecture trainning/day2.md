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
- 可追加4个网段

AWS里没有用broadcast，组播
用R53解决On-premise 服务器与VPC内部server的通信

10.10.0.0 / 16
- .2: DNS
- 10.10.1.0/24
	- 1.0: NV
	- 1.1: Gateway
	- 1.2: DNS relay
	- 1.3: reserved
	- 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk3MzcyMTQ5LC0xMzE5OTAzNzYzLDQyND
M5MzU4MywxODM4NTE2NzQ1XX0=
-->