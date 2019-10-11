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

### System Manager
### OpsWorks
### Elastic Beanstalk


<!--stackedit_data:
eyJoaXN0b3J5IjpbMjAxOTY2MzE4NCwtNzYwMjE0NzE0LC0xMz
UxNDEzNTI5LC0xNDAyMTU4MzgzLDEwOTIyNDY2NzUsLTI4Mzk2
ODExMyw2NjUyMjk0NjcsMTc4MTQ3Njc0NCwtNzIyNzU5MTk2LD
Y4NjgxNzgzNiw0NDE5NDE1NiwtMjE0MDU2NjI3NV19
-->