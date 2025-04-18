---
layout: page
title: Data Object - ADUserInfo
hide:
#  - navigation
  - toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.users.ADUserOrGroup.ADUserInfo`

See also
> [ADGroupInfo](vdi.users.ADUserOrGroup.ADGroupInfo.md)

Since
> Horizon 7.11


## Data Object Description

Info for AD user.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**userSid**|  xsd:string|  Security id of user.
**userGuid**|  xsd:string|  GUID of the user in RFC 4122 format. For e.g. 5F5A45D9-15C0-4654-8FCF-D589C0EF3ECA
**groupInfo**| [ADGroupInfo[]](vdi.users.ADUserOrGroup.ADGroupInfo.md)|  Info for ADGroups of the user. [^1]
**username**|  xsd:string|  The username of user. [^1]
**userPrincipalName**|  xsd:string|  The UPN of user. [^1]
**domain**|  xsd:string|  The domain of user. [^1]
**groupSids**|  xsd:string[]|  The user's groups sids [^1]
 


 


[^1]: This property need not be set.