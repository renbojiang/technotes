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

10.10.0.0 / 16
- .2: DNS
- 10.10.1.0/24
	- 1.0: NV
	- 1.1: Gateway
	- 1.2: DNS relay
	- 1.3: 
<!--stackedit_data:
eyJoaXN0b3J5IjpbNTQ1Mzg5NjUxLC0xMzE5OTAzNzYzLDQyND
M5MzU4MywxODM4NTE2NzQ1XX0=
-->