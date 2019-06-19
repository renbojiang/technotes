# AWS - CI On Boarding

## Guidelines

- [Autodesk Cloud Policies](https://wiki.autodesk.com/display/DOJO/Autodesk+Cloud+Policies)
- [AWS Standard for Cloud Environment](https://wiki.autodesk.com/display/DOJO/AWS+Standards+for+Cloud+Environments)
- 

### Resource-Admin (Resource Administrator)

Resource-Admin is intended for team leaders who manage resources in the integrated account. It provides broad rights for an administrator to manage any resource in an integrated account regardless of its tags or lack of tags. These permissions allow a resource administrator to fix things across the account, and to override other restrictions to ensure that account resources are being used correctly. For example, a resource user can:

-   Respectfully modify any monikered service stack in the account including both registered-monikered and "X"-monikered resources
-   Remove stale EC2 resources, volumes, snapshots, and so on
-   Manage and restrict database sizing
-   Work with beta-grade AWS services that aren't compatible with "Common-IC" security and tagging practices

The resource administrator role is not for performing standard development tasks nor for handling network or security administration. Users should only assume this role on an as-needed basis.

### IAM-Admin (Identity and Access Management Administrator)

IAM-Admin is intended for team leaders who manage users and rights in the integrated account. It deliberately segregates IAM management from resource management to ensure the isolation and integrity required to keep customer data safe. While this isn't important in development and staging, it is very important in production. Having this role in place among all security environments creates a production-compatible practice throughout.

IAM-Admin users can:

-   Change policies
-   Modify trust relationships
-   Create new roles

These capabilities can hone rights and create focused trust relationships that make applications more secure. This role can expand rights, which can endanger security if used the wrong way. We expect all IAM administrators to operate within secure bounds.

IAM admins should _not_:

-   Create new roles with IAM management privileges
-   Create or manage any AWS resource. That privilege is reserved for the resource administrator role.
-   Create new users or manage user keys. These changes are requested through ServiceNow.

In some cases an application may need specialized IAM scripting to be set up. It's best to define this capability using CloudFormation with input variables to adapt to each specific security environment. The IAM-Admin role is more open in the development environment so that IAM operations can be a static setup prior to deployment. When an application moves into staging and production environments, IAM Admin is further locked down.

### Network-Admins (Network Administrator)

Network-Admins is intended for DevOps users who manage and change an integrated account's network configuration. Network-Admins users can create VPCs and work on Route53 and DirectConnect.


1. Apply tag `adsk:moniker` tag (value is `ACADCI-C-UW2`) to all resources you created in MCP VPC.
more details about togging policy: 


## References

### Autodesk Wiki
- [AWS Resource Management Guidelines](https://wiki.autodesk.com/display/DOJO/AWS+Resource+Management+Guidelines)
- [Security Roles](https://wiki.autodesk.com/display/DOJO/Integrated+Account+Security+Roles)
- [Getting Started on Vault](https://wiki.autodesk.com/display/DOJO/Getting+Started+on+HCVault#tab-HC+Vault+CLI)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwNzQ2OTU0MCwtODMyMTQ1NjY4LDE3Nj
MxNDQ4NzYsNzQyNzI5ODYsODc5MjIwNjY2XX0=
-->