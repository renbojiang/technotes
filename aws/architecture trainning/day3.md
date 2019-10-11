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
beanstalk 是学习cloud formation的最好方式

三明治安全模型
R53 -> WAF -> CloudFormation -> ELB -> WAF( third party) -> ELB -> Web App


SQS
AutoScaling 监控的是queue的深度
如果消息过大，建议放进s3，然后发送消息到SQS


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTkxMDM5NTMxMSwyNzEyNzgwMTksODg4Mj
g5MTUsMjAxOTY2MzE4NCwtNzYwMjE0NzE0LC0xMzUxNDEzNTI5
LC0xNDAyMTU4MzgzLDEwOTIyNDY2NzUsLTI4Mzk2ODExMyw2Nj
UyMjk0NjcsMTc4MTQ3Njc0NCwtNzIyNzU5MTk2LDY4NjgxNzgz
Niw0NDE5NDE1NiwtMjE0MDU2NjI3NV19
-->