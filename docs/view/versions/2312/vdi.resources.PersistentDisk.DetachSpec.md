---
layout: page
title: Data Object - PersistentDiskDetachSpec
hide:
#- navigation
- toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.resources.PersistentDisk.DetachSpec`

Parameter to
> [PersistentDisk_Detach](vdi.resources.PersistentDisk.md#detach)

See also
> [DatastorePathId](vdi.entity.DatastorePathId.md)

Since
> Horizon View 6.0


## Data Object Description

**Deprecated.**_This is being deprecated since View Composer will no longer be supported from Horizon version 2012 onwards._

The specification for detaching a persistent disk from a machine.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**archiveDatastorePath**| [DatastorePathId](vdi.entity.DatastorePathId.md)|  The datastore path to archive the virtual disk to. [^1]


 


[^1]: This property need not be set.