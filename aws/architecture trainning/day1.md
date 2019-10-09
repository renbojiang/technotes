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
- ACL主要控制人tong

<!--stackedit_data:
eyJoaXN0b3J5IjpbMzg3NTM5ODAxLC0xNzgyMzgzMzAxLDE2OT
U5ODU0MSwtMzc5Nzg5MTM3LDY3NTQ4NzU2LC0xNzgyMDMyNjk5
LDE0MDAzMjY2MTcsNzMwOTk4MTE2XX0=
-->