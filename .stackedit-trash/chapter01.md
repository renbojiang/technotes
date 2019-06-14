## System Operations
### What's Sys Ops
![system operations](ref/sys_ops.png)

System Operations includes, but is not limited to, the following areas: 
- Network configuration and management
- Server configuration and deployment
- Application deployment and management
- Storage, backup, and archive
- Monitoring
- Security (AWS)

## Sys Ops Activities
![System Ops Activities](ref/sys_ops_activities.png)

When we talk about system operations, we are specifically referring to the following activities.

**Create**
- Development of reusable infrastructure templates 
    - As Unix scripts, programs, CloudFormation templates
- Automated configuration of server instances 
    - EC2 user data, Configuration Management systems (e.g., Chef)
- Storage and archiving of enterprise data 
- Configure domains and routing 

**Deploy** 
- ReDeployment of highly available systems 
- Replication of environments across regions 
- Deployment of dev/test environments
    - Easily de-activated when no longer in use (AWS)
    
**Monitor**
-	Maintenance and patching of running servers
-	Logging and monitoring of system activity
-	Automated reclamation of unused or under-utilized resources (e.g., defining an Amazon Cloudwatch alarm to alert when an instance has had minimal CPU utilization for x number of days, and automatically stop that instance)
-	Scaling of systems to meet on-demand capacity

**Change**
-	Deploying new versions of existing systems (e.g., “blue/green” deployments) (AWS)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjExMTY1NzE5XX0=
-->