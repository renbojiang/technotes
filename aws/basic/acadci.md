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
- One VPC
- Security Group
	- Default: no inbound/outbound rule
	- ACADCI-dev_Dev_Base_Linux_SG
		- inbound: 22
		- 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyOTQ3ODcxMDYsOTgxNDQ2Mjk1LDk5MD
k5Nzk5NCwtMjA3NDY5NTQwLC04MzIxNDU2NjgsMTc2MzE0NDg3
Niw3NDI3Mjk4Niw4NzkyMjA2NjZdfQ==
-->