# Day 1
## Module 1

### AWS Infrastructure

 - [https://www.infrastructure.aws/](https://www.infrastructure.aws/)
 - 全球3个management partition。美国政府，中国及全球
 - delay between AZ is: 2 ms 
 - AZ做双活高可用，Region做灾备
 - 计费模式不可忽略
 - 各个AZ其实是随机值。

### Edge Location
 #### Performance
	 - R53
		 - 全球DNS解析服务
		 - 内部DNS解析
		 - 不同的路由选择策略
		 - 服务发现
	 - CloudFront: CDN
 #### Security
	 - Shield
		 - DDos
	 - WAF
		 - 应用层防火墙
#### 全托管服务

# Module 2
### S3
- Object-level storage (vs. block storage)
- 99.99% (4个9) availability , 99.9.. 9% (11个9) durability
- Event Trigger 
- S3是global service，但S3 bucket必须属于某个region。Bucket 名字management partition唯一。 arn命名规则决定的。
- 

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTY5NTk4NTQxLC0zNzk3ODkxMzcsNjc1ND
g3NTYsLTE3ODIwMzI2OTksMTQwMDMyNjYxNyw3MzA5OTgxMTZd
fQ==
-->