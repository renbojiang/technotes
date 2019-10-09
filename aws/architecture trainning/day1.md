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
- 可以方便实现托管静态站点
- 主要存放非结构化数据
- 不具备stream数据输入

**ACL**
- 两级ACL： Object， Bucket 
- 默认阻止所有公共访问权限
- ACL主要控制人通过internet来访问S3的权限控制。 通过API来访问的控制，主要通过Role。
- 公开一个对象，是针对对象，而不是针对对象URL

**Bucket Policy**
- 实现更精细的访问控制，比如可以限制从哪里来的访问控制
- Policy可以通过template统一部署

**AWS Policy 有两类：**
- Identity Policy
- Resource Policy

**Versioning Control**
- 默认不开启bucket的versioning control
- 可以通过带版本信息的URL访问各个版本的对象
- 区别删除一个对象（marked it as deleted, a new version）和删除某个版本的对象

**Access control - CORS**
- 可自定义CORS策略

**Upload/Download**
- Multipart Upload 多路并行上传
- Global Accelerate (Edge location: CloudFront)
- Snowball 快递 / Snowmobile 集装箱

**收费**
- Storage: $0.023GB/Month
- Transfer out: to other region or internet. $0.09/GB
- API calls: 不要将零散的平凡访问的数据放进S3
https://aws.amazon.com/cn/s3/pricing

**存储方式**
- 通过数据访问频度选择存储方式
- S3 standard -> IA -> Glacier
- 操作
	- Life Cycle Rules
	- Lambda自定义策略
	- 更改存储类 （智能分层）

**Glacier**
- 库锁 Vault Lock
- 存储存档数据
- Restore的时间一般为2~3小时

## Module 3

**EC2**
- 一次性计算资源 
- 不保存状态信息

**AMI**
- AMI includes
	- A template for the root volume
	- Launch permissions
	- a block device mapping
	
**选择AMI**
	- x86/arm
	- hvm / pv
	- 64bit / 32 bit
	- OS
		- charge for seconds
			- Amazon Linux
			- Ubuntu
		- charge for hours
	- Launch Permission (Golden Image)

**EC2 Storage**
- EBS (Elastic Block Store)
	- snapshot (保存进S3）
	- 不在EBS里保存重要信息
	- 和EC2不在一个主机上，通过网络互连
- Instance storage
	- 和EC2在一个主机上
	- 易失性 （随EC2）

SSD
- General Purpose SSD
- IOPS SSD （6400）
- 
**M5.Large**
 - M: family name 
 - 5: generation number 
 - Large: the size of the instance

**T系列**
 - 20%基线
 - credit

**C系列**
- Nitro
- 99.99%裸机性能
- 1：2 cpu：memory

**R系列**
- 1：8 cpu：memory

**P系列**
- 1：8 cpu：memory
- Deep Learning

**H系列**
- instance strorage
- IOPS throughput 优化

**Tips**
- ECU 是性能指标
- 不确定EC2 type的时候，从M系列开始，用cloudwatch观察，然后替换
- IaC: Infrastructure as Code
- EC2 stop/start 一定会换硬件系统，进入一个新的计费周期。但restart不进入新的计费周期。

**User Data**
- User Data是以root身份执行的
- User Data可以通过code deploy发布
- check instance metadata: 
	- ```curl http://169.254.169.254/latest/meta-data/```
	- ```curl http://169.254.169.254/latest/meta-data/instance-type```

**EC2 Pricing Option**
- On-demand
	- 按使用量收费
- Reserved
	- 提前付费（0 ~ full）
	- 12个月 ~ 36个月
	- RI Market
	- 不建议大量购买
	- 开启on-demand时，如果符合Reserved Instance，自动转化为RI
- Spot
	- 20% ~ 30% on-demand price
	- offline notification: 2min by meta-data
	- 竞价休眠模式
- Dedicated Instance
- Dedicated host

**购买建议**
- 以最低维持业务的标准购买RI
- 以spot对付业务激增
- 以On-demand对付增长


<!--stackedit_data:
eyJoaXN0b3J5IjpbNjUxMjE3MDg0LDEwNTAyOTk2NTQsLTE2Mj
MwODIwMzMsMjEyODI1MTM1NiwyMTIwODQ4NTk4LDExMjA1NzEx
MDksMTA0MTYzMzI1OCw1NDgzNTY1MzgsLTgwNzEyMTMyMiwxMj
E0NzI5MjY3LDEzNjQwOTc3MjksLTU5OTIyNDM0Nyw3MjIxNTMx
MzUsLTExMjgwNzU2NDIsNzU1OTQ5NjQzLC00MzQzNzQwNjAsLT
I1NzExOTQwOSwyMDE2OTM3MTUwLDc4ODE0Njc4OCwtMjA3Mjcx
NjY5Nl19
-->