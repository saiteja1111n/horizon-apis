---
layout: page
title: Data Object - NetworkLabelInfo
hide:
#  - navigation
  - toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.utils.virtualcenter.NetworkLabel.NetworkLabelInfo`

Returned by
> [NetworkLabel_ListByHostOrCluster](vdi.utils.virtualcenter.NetworkLabel.md#listByHostOrCluster), [NetworkLabel_ListByNetworkLabelSpec](vdi.utils.virtualcenter.NetworkLabel.md#listByNetworkLabelSpec)

See also
> [NetworkLabelData](vdi.utils.virtualcenter.NetworkLabel.NetworkLabelData.md), [NetworkLabelId](vdi.entity.NetworkLabelId.md)

Since
> Horizon View 6.0


## Data Object Description

Network label information from VC.
 [^167]



## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**id**| [NetworkLabelId](vdi.entity.NetworkLabelId.md)|  Network label id. [^2]
**data**| [NetworkLabelData](vdi.utils.virtualcenter.NetworkLabel.NetworkLabelData.md)|  Network label data. [^2]
**refId**|  xsd:string|  Reference ID used for this network label.  **_Since_** Horizon 8.1 [^1] [^2]


 


[^1]: This property need not be set.
[^2]: This property cannot be updated.
[^167]: This data object must be updated as a whole.