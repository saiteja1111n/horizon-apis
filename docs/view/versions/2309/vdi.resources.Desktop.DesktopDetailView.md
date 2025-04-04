---
layout: page
title: Data Object - DesktopDetailView
hide:
#  - navigation
  - toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.resources.Desktop.DesktopDetailView`

Returned by
> [Desktop_GetDetailView](vdi.resources.Desktop.md#getDetailView)

See also
> [DesktopDetailData](vdi.resources.Desktop.DesktopDetailData.md), [DesktopId](vdi.entity.DesktopId.md)

Since
> Horizon 7.4


## Data Object Description

Desktop id + Desktop Detail data.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**id**| [DesktopId](vdi.entity.DesktopId.md)|  The id of the desktop.
**desktopDetailData**| [DesktopDetailData](vdi.resources.Desktop.DesktopDetailData.md)|  Core attributes of the desktop instance.
**refId**|  xsd:string|  Reference ID used for this desktop pool.  **_Since_** Horizon 8.1 [^1] [^2]
 


 


[^1]: This property need not be set.
[^2]: This property cannot be updated.