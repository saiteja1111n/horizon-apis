---
layout: page
title: Data Object - DesktopManualVirtualMachineDefinition
hide:
#  - navigation
  - toc
---





Java Class
> ` com.omnissa.vdi.vlsi.binding.vdi.resources.Desktop.ManualVirtualMachineDefinition`

Parameter to
> [Desktop_ValidateVmNamesInfo](vdi.resources.Desktop.md#validateVmNamesInfo)

See also
> [DesktopId](vdi.entity.DesktopId.md), [DesktopManualVirtualMachinesSpec](vdi.resources.Desktop.ManualVirtualMachinesSpec.md)

Since
> Horizon 7.4


## Data Object Description

Virtual machine definition used for validating manual configured machines.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**manualVirtualMachinesSpec**| [DesktopManualVirtualMachinesSpec[]](vdi.resources.Desktop.ManualVirtualMachinesSpec.md)|  List of manually defined virtual machines
**id**| [DesktopId](vdi.entity.DesktopId.md)|  ID of the desktop to which the manually defined virtual machines will belong. Only required if virtual machines are being added to an existing pool. [^1]
**isNonPersistentDesktop**|  xsd:boolean|  Indicates whether desktop is persistent or non-persistent. [^5] [^1]


 


[^1]: This property need not be set.
[^5]: This property has a default value of false.