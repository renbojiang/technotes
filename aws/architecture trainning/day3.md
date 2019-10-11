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
主要用来作蓄洪
AutoScaling 监控的是queue的深度
如果消息过大，建议放进s3，然后发送消息到SQS
SWF可以做消息更精细的控制
SQS可以配合SNS做多播


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1MzUyNTk0MzEsLTkxMDM5NTMxMSwyNz
EyNzgwMTksODg4Mjg5MTUsMjAxOTY2MzE4NCwtNzYwMjE0NzE0
LC0xMzUxNDEzNTI5LC0xNDAyMTU4MzgzLDEwOTIyNDY2NzUsLT
I4Mzk2ODExMyw2NjUyMjk0NjcsMTc4MTQ3Njc0NCwtNzIyNzU5
MTk2LDY4NjgxNzgzNiw0NDE5NDE1NiwtMjE0MDU2NjI3NV19
-->