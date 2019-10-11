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
- retain
resource 按照定义顺序来创建

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzNTE0MTM1MjksLTE0MDIxNTgzODMsMT
A5MjI0NjY3NSwtMjgzOTY4MTEzLDY2NTIyOTQ2NywxNzgxNDc2
NzQ0LC03MjI3NTkxOTYsNjg2ODE3ODM2LDQ0MTk0MTU2LC0yMT
QwNTY2Mjc1XX0=
-->