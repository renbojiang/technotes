# AWS - CI On Boarding

## Guidelines

- [Autodesk Cloud Policies](https://wiki.autodesk.com/display/DOJO/Autodesk+Cloud+Policies)
- [AWS Standard for Cloud Environment](https://wiki.autodesk.com/display/DOJO/AWS+Standards+for+Cloud+Environments)
- [Security Roles](https://wiki.autodesk.com/display/DOJO/Integrated+Account+Security+Roles)
- 
1. Apply tag `adsk:moniker` tag (value is `ACADCI-C-UW2`) to all resources you created in MCP VPC.
more details about togging policy: 

2. add ```10.35.136.250 git.autodesk.com``` to ```/etc/hosts```
3. 
## References

### Autodesk Wiki
- [AWS Resource Management Guidelines](https://wiki.autodesk.com/display/DOJO/AWS+Resource+Management+Guidelines)

- [Getting Started on Vault](https://wiki.autodesk.com/display/DOJO/Getting+Started+on+HCVault#tab-HC+Vault+CLI)


## MCP VPC
- VPC
	- IPv4 CIDR: 10.117.192.0/21
	- DHCP Options set:
		- domain-name-servers=AmazonProvidedDNS
		- domain-name=us-west-2.compute.internal
	- 
- Security Group
	- Default: no inbound/outbound rule
	- ACADCI-dev_Dev_Base_Linux_SG
		- inbound: 22 (SSH)
		- outbound: port range listed
	- ACADCI-dev_Dev_Base_Windows_SG
		- inbound: 3389 (Remote Desktop)
		- outbound: port range listed
- 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk4NTgxNjk3LC0xMTk1MzM4Nzg4LDkwNz
gzNzU5MSw5ODE0NDYyOTUsOTkwOTk3OTk0LC0yMDc0Njk1NDAs
LTgzMjE0NTY2OCwxNzYzMTQ0ODc2LDc0MjcyOTg2LDg3OTIyMD
Y2Nl19
-->