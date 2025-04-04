---
layout: page
title: Data Object - AdminUserOrGroupPrivilegesInfo
hide:
#  - navigation
  - toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.users.AdminUserOrGroup.AdminUserOrGroupPrivilegesInfo`

Property of
> [AdminUserOrGroupLoginView](vdi.users.AdminUserOrGroup.AdminUserOrGroupLoginView.md#field_detail)

See also
> [AccessGroupId](vdi.entity.AccessGroupId.md), [AccessGroupSummaryView](vdi.users.AccessGroup.AccessGroupSummaryView.md)

Since
> Horizon 7.5


## Data Object Description

Represents access group and privileges mapping for the user or group.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**accessGroupId**| [AccessGroupId](vdi.entity.AccessGroupId.md)|  The access group id.
**accessGroupName**|  xsd:string|  The access group name.
**privileges**|  xsd:string[]|  The set of privileges on the current access group.
**children**| [AccessGroupSummaryView[]](vdi.users.AccessGroup.AccessGroupSummaryView.md)|  Child access groups associated with current access group.  **_Since_** Horizon 7.6 [^1]
 


 


[^1]: This property need not be set.