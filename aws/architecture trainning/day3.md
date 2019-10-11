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


<!--stackedit_data:
eyJoaXN0b3J5IjpbMjcxMjc4MDE5LDg4ODI4OTE1LDIwMTk2Nj
MxODQsLTc2MDIxNDcxNCwtMTM1MTQxMzUyOSwtMTQwMjE1ODM4
MywxMDkyMjQ2Njc1LC0yODM5NjgxMTMsNjY1MjI5NDY3LDE3OD
E0NzY3NDQsLTcyMjc1OTE5Niw2ODY4MTc4MzYsNDQxOTQxNTYs
LTIxNDA1NjYyNzVdfQ==
-->