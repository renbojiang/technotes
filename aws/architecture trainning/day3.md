# Day 3
## IAM
**IAM Policy**
-> Deny -> Allow -> Default(deny)

**Signature Version 4**
http://169.254.169.254/latest/meta-data/iam/info
http://169.254.169.254/latest/meta-data/iam/security-credentials/...

**Cognito**

## Automation
一旦开始自动化，绝不要做任何手工操作/配置

### CloudFormation
**cloud formation elements**
- parameters
- map
- condition
- depend on: 非强制依赖
- ref：强制依赖
resource 按照定义顺序来创建

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0MDIxNTgzODMsMTA5MjI0NjY3NSwtMj
gzOTY4MTEzLDY2NTIyOTQ2NywxNzgxNDc2NzQ0LC03MjI3NTkx
OTYsNjg2ODE3ODM2LDQ0MTk0MTU2LC0yMTQwNTY2Mjc1XX0=
-->