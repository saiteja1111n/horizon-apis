---
layout: page
title: Data Object - DesktopCustomizationScriptSettings
hide:
#  - navigation
  - toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.resources.Desktop.CustomizationScriptSettings`

Property of
> [DesktopCustomizationSettings](vdi.resources.Desktop.CustomizationSettings.md#field_detail)

Since
> Horizon 8.11


## Data Object Description

Customization scripts to run on a cloned VM.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**powerOffScriptName**|  xsd:string|  Power off script. Allows to run a customization script on cloned machines before they are powered off. Provide the path to the script on the parent virtual machine. [^1]
**powerOffScriptParameters**|  xsd:string|  Power off script parameters. Example: p1 p2 p3 [^1]
**postSynchronizationScriptName**|  xsd:string|  Post synchronization script. Allows to run a customization script on cloned machines after they are created, recomposed, or refreshed. Provide the path to the script on the parent virtual machine. [^1]
**postSynchronizationScriptParameters**|  xsd:string|  Post synchronization script parameters. Example: p1 p2 p3 [^1]


 


[^1]: This property need not be set.