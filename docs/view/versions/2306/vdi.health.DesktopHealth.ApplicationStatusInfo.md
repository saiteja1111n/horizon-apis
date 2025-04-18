---
layout: page
title: Data Object - ApplicationStatusInfo
hide:
#  - navigation
  - toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.health.DesktopHealth.ApplicationStatusInfo`

Property of
> [DesktopHealthInfo](vdi.health.DesktopHealth.DesktopHealthInfo.md#field_detail)

See also
> [ApplicationId](vdi.entity.ApplicationId.md)

Since
> Horizon View 6.0


## Data Object Description

Status of applications created from desktop.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**id**| [ApplicationId](vdi.entity.ApplicationId.md)|  Application Entity Id [^2]
**status**|  xsd:string|  Application Status [^2]<br>* This property will be one of:<br><table><tr><th>Value</th><th>Description</th></tr><tr><td>"AVAILABLE"</td><td>The application is available in all machines of the desktop.</td></tr><tr><td>"MISSING"</td><td>The application is missing in one or more machines in the desktop.</td></tr><tr><td>"UNAVAILABLE"</td><td>Could happen in any of following cases: [^235] [^236]</td></tr><tr><td>"DISABLED"</td><td>The desktop is disabled and the application is disabled.</td></tr></table>
 


 


[^2]: This property cannot be updated.
[^235]: The application is missing in all the machines of the desktop.
[^236]: Desktop do not have any provisioned machines.