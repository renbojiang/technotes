

# Day 1
## AWS Infrastructure

 - [https://www.infrastructure.aws/](https://www.infrastructure.aws/)
 - 全球3个management partition。美国政府，中国及全球
 - delay between AZ is: 2 ms 
 - AZ做双活高可用，Region做灾备
 - 计费模式不可忽略
 - 各个AZ其实是随机值。

### Edge Location
 - Performance
	 - R53
		 - 全球DNS解析服务
		 - 内部DNS解析
		 - 不同的路由选择策略
		 - 服务发现
	 - CloudFront: CDN
 - Security
	 - Shield
		 - DDos
	 - WAF
		 - 应用层防火墙

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc1MzY2MTc4Niw2NzU0ODc1NiwtMTc4Mj
AzMjY5OSwxNDAwMzI2NjE3LDczMDk5ODExNl19
-->