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
- S3是global service，但S3 bucket必须属于某个region。
- Bucket 名字是management partition唯一。 arn命名规则决定的。
- S3对象命名：bucket.s3-region.amazonaws.com/object 或者 s3-region.amazonaws.com/bucket/object ，注意US East没有region名称。
- S3对象的键值总是包含路劲的。

**ACL**
- 两级ACL： Object， Bucket 
- 默认阻止所有公共访问权限
- ACL主要控制人通过internet来访问S3的权限控制。 通过API来访问的控制，主要通过Role。

**Bucket Policy**
- 实现更精细的访问控制，比如可以限制从哪里来的访问控制

**AWS Policy 有两类：**
- Identity Policy
- Resource Policy

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY4NjU3OTAzMSwtMTc5OTgxMjYzMCwtMT
c4MjM4MzMwMSwxNjk1OTg1NDEsLTM3OTc4OTEzNyw2NzU0ODc1
NiwtMTc4MjAzMjY5OSwxNDAwMzI2NjE3LDczMDk5ODExNl19
-->