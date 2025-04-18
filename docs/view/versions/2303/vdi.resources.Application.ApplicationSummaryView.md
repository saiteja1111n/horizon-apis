---
layout: page
title: Data Object - ApplicationSummaryView
hide:
#  - navigation
  - toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.resources.Application.ApplicationSummaryView`

Returned by
> [Application_GetSummaryView](vdi.resources.Application.md#getSummaryView), [Application_GetSummaryViews](vdi.resources.Application.md#getSummaryViews), [Application_ListGAECompatibleApplications](vdi.resources.Application.md#listGAECompatibleApplications)

See also
> [ApplicationId](vdi.entity.ApplicationId.md), [ApplicationSummaryData](vdi.resources.Application.ApplicationSummaryData.md)

Since
> Horizon 7.2


## Data Object Description

Application Summary View.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**id**| [ApplicationId](vdi.entity.ApplicationId.md)|  Application id.
**applicationSummaryData**| [ApplicationSummaryData](vdi.resources.Application.ApplicationSummaryData.md)|  Application Summary Data.
**refId**|  xsd:string|  Reference ID used for this application pool.  **_Since_** Horizon 8.1 [^1] [^2]
 


 


[^1]: This property need not be set.
[^2]: This property cannot be updated.