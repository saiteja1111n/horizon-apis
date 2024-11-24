---
layout: page
title: Data Object - QueryFilterEquals
hide:
#- navigation
- toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.query.QueryFilter.Equals`

Extends
> [QueryFilter](vdi.query.QueryFilter.Filter.md)

Since
> Horizon View 6.0


## Data Object Description

Specify that the named member must be equal to the specified value. The supported types are:

* xsd:string: The value in the resulting data object must be equal to the specified [value](vdi.query.QueryFilter.Equals.md#value), ignores case.
* xsd:ArrayOfString: The values in the resulting data object must be equal to the specified [value](vdi.query.QueryFilter.Equals.md#value), ignores case.
* Object: The values in the resulting data object must be equal to the specified [value](vdi.query.QueryFilter.Equals.md#value). This equality is based on object's equals method implementation

 [^167]



## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**memberName**|  xsd:string|  The name of the member to compare.
**value**|  xsd:anyType|  The value to be compared against. [^1]
Properties inherited from [QueryFilter](vdi.query.QueryFilter.Filter.md)
None


 


[^1]: This property need not be set.
[^167]: This data object must be updated as a whole.