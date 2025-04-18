---
layout: page
title: Data Object - ImageManagementStreamInfo
hide:
#  - navigation
  - toc
---





Java Class
> ` com.omnissa.vdi.vlsi.binding.vdi.utils.imagemanagement.ImageManagementStream.ImageManagementStreamInfo`

Returned by
> [ImageManagementStream_Get](vdi.utils.imagemanagement.ImageManagementStream.md#get), [ImageManagementStream_ListBySpec](vdi.utils.imagemanagement.ImageManagementStream.md#listBySpec)

See also
> [ImageManagementStreamBase](vdi.utils.imagemanagement.ImageManagementStream.ImageManagementStreamBase.md), [ImageManagementStreamId](vdi.entity.ImageManagementStreamId.md)

Since
> Horizon 7.10


## Data Object Description

Top level object describing a image management stream.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**id**| [ImageManagementStreamId](vdi.entity.ImageManagementStreamId.md)|  Entity id of image management stream. [^2]
**base**| [ImageManagementStreamBase](vdi.utils.imagemanagement.ImageManagementStream.ImageManagementStreamBase.md)|  Basic data about a image management stream.
**refId**|  xsd:string|  Reference ID used for this image management stream.  **_Since_** Horizon 8.1 [^1] [^2]


 


[^1]: This property need not be set.
[^2]: This property cannot be updated.