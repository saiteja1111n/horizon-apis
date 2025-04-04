---
layout: page
title: Data Object - VirtualCenterHealthDatastoreData
hide:
#  - navigation
  - toc
---





Java Class
> ` com.omnissa.vdi.vlsi.binding.vdi.health.VirtualCenterHealth.DatastoreData`

Property of
> [VirtualCenterHealthInfo](vdi.health.VirtualCenterHealth.VirtualCenterHealthInfo.md#field_detail)

See also
> [DatastoreId](vdi.entity.DatastoreId.md)

Since
> Horizon View 6.0


## Data Object Description

Health information about a Virtual Center datastore.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**id**| [DatastoreId](vdi.entity.DatastoreId.md)|  The ID of the Datastore.  **_Since_** Horizon 7.9
**name**|  xsd:string|  The name of the datastore.
**accessible**|  xsd:boolean|  Whether or not this data store is accessible [^1]
**path**|  xsd:string|  The path to the datastore. [^1]
**datastoreType**|  xsd:string|  The type of the datastore. [^1]
**capacityMB**|  xsd:long|  The capacity of the datastore in megabytes. [^1]
**freeSpaceMB**|  xsd:long|  The free space on the datastore in megabytes. [^1]
**url**|  xsd:string|  The unique locator for the datastore.  **_Since_** Horizon 7.7 [^1]


 


[^1]: This property need not be set.