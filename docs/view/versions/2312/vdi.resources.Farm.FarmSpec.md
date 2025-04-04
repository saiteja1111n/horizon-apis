---
layout: page
title: Data Object - FarmSpec
hide:
#  - navigation
  - toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.resources.Farm.FarmSpec`

Parameter to
> [Farm_Create](vdi.resources.Farm.md#create)

See also
> [FarmAutomatedFarmSpec](vdi.resources.Farm.AutomatedFarmSpec.md), [FarmData](vdi.resources.Farm.FarmData.md), [FarmManualFarmSpec](vdi.resources.Farm.ManualFarmSpec.md)

Since
> Horizon View 6.2


## Data Object Description

Farm spec data needed to create a Farm

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**type**|  xsd:string|  Type of farm. <br>* This property will be one of:<br><table><tr><th>Value</th><th>Description</th></tr><tr><td>"AUTOMATED"</td><td>An automated farm creates RDS Servers cloned from a snapshot.</td></tr><tr><td>"MANUAL"</td><td>A manual farm allows selection and addition of existing RDS Servers to the farm.</td></tr></table>
**data**| [FarmData](vdi.resources.Farm.FarmData.md)|  Farm data
**automatedFarmSpec**| [FarmAutomatedFarmSpec](vdi.resources.Farm.AutomatedFarmSpec.md)|  Automated farm spec. [^1] [^29]
**manualFarmSpec**| [FarmManualFarmSpec](vdi.resources.Farm.ManualFarmSpec.md)|  Manual Farm spec [^1] [^26]


 


[^1]: This property need not be set.
[^26]: This property is required if type is set to 'MANUAL'.
[^29]: This property is required if type is set to 'AUTOMATED'.