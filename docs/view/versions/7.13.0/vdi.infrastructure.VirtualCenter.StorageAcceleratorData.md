---
layout: page
title: Data Object - VirtualCenterStorageAcceleratorData
hide:
#  - navigation
  - toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.infrastructure.VirtualCenter.StorageAcceleratorData`

Property of
> [VirtualCenterInfo](vdi.infrastructure.VirtualCenter.VirtualCenterInfo.md#field_detail), [VirtualCenterSpec](vdi.infrastructure.VirtualCenter.VirtualCenterSpec.md#field_detail)

See also
> [VirtualCenterStorageAcceleratorHostOverride](vdi.infrastructure.VirtualCenter.StorageAcceleratorHostOverride.md)

Since
> Horizon View 6.0


## Data Object Description

View Storage Accelerator configuration details.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**enabled**|  xsd:boolean|  Is View Storage Accelerator enabled? [^5]
**defaultCacheSizeMB**|  xsd:int|  Default size of the cache in megabytes. [^176] [^1] [^177] [^178] [^53]
**hostOverrides**| [VirtualCenterStorageAcceleratorHostOverride[]](vdi.infrastructure.VirtualCenter.StorageAcceleratorHostOverride.md)|  Cache size overrides for hosts which support View Storage Accelerator. [^1]


 


[^1]: This property need not be set.
[^5]: This property has a default value of false.
[^53]: This property is required if enabled is set to true.
[^176]: This property has a default value of 1024.
[^177]: This property has a minimum value of 100.
[^178]: This property has a maximum value of 32768.