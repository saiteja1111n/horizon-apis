---
layout: page
title: Data Object - FarmVirtualCenterProvisioningSettings
hide:
#  - navigation
  - toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.resources.Farm.VirtualCenterProvisioningSettings`

Property of
> [FarmAutomatedFarmData](vdi.resources.Farm.AutomatedFarmData.md#field_detail), [FarmAutomatedFarmSpec](vdi.resources.Farm.AutomatedFarmSpec.md#field_detail)

See also
> [FarmVirtualCenterNetworkingSettings](vdi.resources.Farm.VirtualCenterNetworkingSettings.md), [FarmVirtualCenterProvisioningData](vdi.resources.Farm.VirtualCenterProvisioningData.md), [FarmVirtualCenterStorageSettings](vdi.resources.Farm.VirtualCenterStorageSettings.md)

Since
> Horizon View 6.2


## Data Object Description

Virtual Center entities associated with this Automated farm.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**enableProvisioning**|  xsd:boolean|  Whether to enable provisioning immediately. [^6]
**stopProvisioningOnError**|  xsd:boolean|  Whether provisioning on all VMs stops on error. [^6]
**minReadyVMsOnVComposerMaintenance**|  xsd:int|  Minimum number of ready (provisioned) RDS Servers during Instant clone maintenance operations. Use this setting to perform machine maintenance operations in a rolling fashion. Increasing this count may decrease the concurrency for Instant clone maintenance operations for the automated farm. This is applicable in the case of instant-clone Automated farm. [^19] [^72]
**virtualCenterProvisioningData**| [FarmVirtualCenterProvisioningData](vdi.resources.Farm.VirtualCenterProvisioningData.md)|  Virtual center entities used for provisioning.
**virtualCenterStorageSettings**| [FarmVirtualCenterStorageSettings](vdi.resources.Farm.VirtualCenterStorageSettings.md)|  Virtual Center storage settings.
**virtualCenterNetworkingSettings**| [FarmVirtualCenterNetworkingSettings](vdi.resources.Farm.VirtualCenterNetworkingSettings.md)|  Virtual Center networking settings.


 


[^6]: This property has a default value of true.
[^19]: This property has a default value of 0.
[^72]: This property has a minimum value of 0.