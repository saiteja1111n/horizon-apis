---
layout: page
title: Service - LogCollector
hide:
#  - navigation
  - toc
---







Java Class
> ` com.omnissa.vdi.vlsi.binding.vdi.utils.logcollector.LogCollector`

See also
> [LogCollectorComponentIdentifier](vdi.utils.logcollector.LogCollector.LogCollectorComponentIdentifier.md), [LogCollectorDownloadURLInfo](vdi.utils.logcollector.LogCollector.LogCollectorDownloadURLInfo.md), [LogCollectorSpec](vdi.utils.logcollector.LogCollector.LogCollectorSpec.md), [LogCollectorTaskId](vdi.entity.LogCollectorTaskId.md), [LogCollectorTaskInfo](vdi.utils.logcollector.LogCollector.LogCollectorTaskInfo.md), [LogLevelInfo](vdi.utils.logcollector.LogCollector.LogLevelInfo.md), [LogLevelSpec](vdi.utils.logcollector.LogCollector.LogLevelSpec.md), [UserOrGroupId](vdi.entity.UserOrGroupId.md)

Since
> Horizon 7.10





## Service Description

Service Interface for collecting DCT bundle from Connector Server.

**Methods**

Methods defined in this Service:
LogCollector_Clean, LogCollector_Collect, LogCollector_GetDownloadURL, LogCollector_GetLogLevels, LogCollector_GetTaskInfo, LogCollector_GetTaskInfoById, LogCollector_List, LogCollector_Purge, LogCollector_SetLogLevels




A finish acknowledgement to notify the connection server for cleanup of collect complete log bundles or to terminate the collect operation if is in progress of collecting logs bundle.

**Privileges**

Privilege | Description
:---|:---
LOG_COLLECTION|  Log collection privilege is required to perform log collection operations.



**Parameters**

 Name | Type | Description
:---|:---|:---
**_this**| [ManagedObjectReference](vmodl.ManagedObjectReference.md)|  A reference to the [LogCollector](vdi.utils.logcollector.LogCollector.md) used to make the method call.
**logCollectorTaskIdList**| [LogCollectorTaskId[]](vdi.entity.LogCollectorTaskId.md)|




**Return Value**

Type | Description
:---|:---
None



**Faults**

Type | Description
:---|:---
[EntityNotFound](vdi.fault.EntityNotFound.md)| Thrown if any specified entity cannot be found.
[InsufficientPermission](vdi.fault.InsufficientPermission.md)| Thrown if the user does not have sufficient permission to perform the operation.
[InvalidArgument](vdi.fault.InvalidArgument.md)| Thrown if any specified argument is invalid.
[InvalidType](vdi.fault.InvalidType.md)| Thrown if the type of any specified argument is invalid.
[PartialFailureFault](vdi.fault.PartialFailureFault.md)| [^159] [^160]
[UnexpectedFault](vdi.fault.UnexpectedFault.md)| Thrown if an unexpected error occurs while performing the operation.



**Events**

Event | Description
:---|:---
VLSI_LOG_COLLECTION_PURGE_TASK_SUCCESS|  \- Generated for each of the log component type when the log purge request is successfully submitted
VLSI_LOG_COLLECTION_ABORT_TASK_SUCCESS|  \- Generated for each of the log component type when the log abort request is successfully submitted

Show WSDL type definition







Sends the log collection request for the set of targets

**Privileges**

Privilege | Description
:---|:---
LOG_COLLECTION|  Log collection privilege is required to perform log collection operations.



**Parameters**

 Name | Type | Description
:---|:---|:---
**_this**| [ManagedObjectReference](vmodl.ManagedObjectReference.md)|  A reference to the [LogCollector](vdi.utils.logcollector.LogCollector.md) used to make the method call.
**logCollectorSpecList**| [LogCollectorSpec[]](vdi.utils.logcollector.LogCollector.LogCollectorSpec.md)|




**Return Value**

Type | Description
:---|:---
[LogCollectorTaskInfo[]](vdi.utils.logcollector.LogCollector.LogCollectorTaskInfo.md)| Array of [LogCollectorTaskInfo](vdi.utils.logcollector.LogCollector.LogCollectorTaskInfo.md) \- A unique task id is returned as part of each LogCollectorTaskInfo. It is responsibility of the caller to keep track of it for using it later for fetching the status of it.



**Faults**

Type | Description
:---|:---
[EntityNotFound](vdi.fault.EntityNotFound.md)| Thrown if any specified entity cannot be found.
[InsufficientPermission](vdi.fault.InsufficientPermission.md)| Thrown if the user does not have sufficient permission to perform the operation.
[InvalidArgument](vdi.fault.InvalidArgument.md)| Thrown if any specified argument is invalid.
[InvalidType](vdi.fault.InvalidType.md)| Thrown if the type of any specified argument is invalid.
[PartialFailureFault](vdi.fault.PartialFailureFault.md)| [^161] [^160]
[UnexpectedFault](vdi.fault.UnexpectedFault.md)| Thrown if an unexpected error occurs while performing the operation.



**Events**

Event | Description
:---|:---
VLSI_LOG_COLLECTION_INITIATE_TASK_SUCCESS|  \- Generated for each of the log component type when the log collect request is successfully submitted

Show WSDL type definition







Retrieves Download URL for each of specified [LogCollectorTaskId](vdi.entity.LogCollectorTaskId.md)

**Privileges**

Privilege | Description
:---|:---
LOG_COLLECTION|  Log collection privilege is required to perform log collection operations.



**Parameters**

 Name | Type | Description
:---|:---|:---
**_this**| [ManagedObjectReference](vmodl.ManagedObjectReference.md)|  A reference to the [LogCollector](vdi.utils.logcollector.LogCollector.md) used to make the method call.
**logCollectorTaskIdList**| [LogCollectorTaskId[]](vdi.entity.LogCollectorTaskId.md)|




**Return Value**

Type | Description
:---|:---
[LogCollectorDownloadURLInfo[]](vdi.utils.logcollector.LogCollector.LogCollectorDownloadURLInfo.md)| Array of [LogCollectorDownloadURLInfo](vdi.utils.logcollector.LogCollector.LogCollectorDownloadURLInfo.md)



**Faults**

Type | Description
:---|:---
[EntityNotFound](vdi.fault.EntityNotFound.md)| Thrown if any specified entity cannot be found.
[InsufficientPermission](vdi.fault.InsufficientPermission.md)| Thrown if the user does not have sufficient permission to perform the operation.
[InvalidArgument](vdi.fault.InvalidArgument.md)| Thrown if any specified argument is invalid.
[InvalidType](vdi.fault.InvalidType.md)| Thrown if the type of any specified argument is invalid.
[PartialFailureFault](vdi.fault.PartialFailureFault.md)| [^161] [^160]
[UnexpectedFault](vdi.fault.UnexpectedFault.md)| Thrown if an unexpected error occurs while performing the operation.



**Events**

Event | Description
:---|:---
VLSI_LOG_COLLECTION_DOWNLOAD_TASK_SUCCESS|  \- Generated for each of the log component type when log download URL is retrieved successfully

Show WSDL type definition







Fetches feature wise log level information for a component.

**Privileges**

Privilege | Description
:---|:---
LOG_COLLECTION|  Log collection privilege is required to perform log collection operations.



**Parameters**

 Name | Type | Description
:---|:---|:---
**_this**| [ManagedObjectReference](vmodl.ManagedObjectReference.md)|  A reference to the [LogCollector](vdi.utils.logcollector.LogCollector.md) used to make the method call.
**logCollectorComponentId**| [LogCollectorComponentIdentifier](vdi.utils.logcollector.LogCollector.LogCollectorComponentIdentifier.md)|




**Return Value**

Type | Description
:---|:---
[LogLevelInfo](vdi.utils.logcollector.LogCollector.LogLevelInfo.md)| [LogLevelInfo](vdi.utils.logcollector.LogCollector.LogLevelInfo.md) \- Contains feature-wise log level information for a component



**Faults**

Type | Description
:---|:---
[EntityNotFound](vdi.fault.EntityNotFound.md)| Thrown if any specified entity cannot be found.
[InsufficientPermission](vdi.fault.InsufficientPermission.md)| Thrown if the user does not have sufficient permission to perform the operation.
[InvalidArgument](vdi.fault.InvalidArgument.md)| Thrown if any specified argument is invalid.
[InvalidType](vdi.fault.InvalidType.md)| Thrown if the type of any specified argument is invalid.
[LogCollectorFault](vdi.fault.LogCollectorFault.md)| Thrown if the getLogLevels fails for the given component.
[UnexpectedFault](vdi.fault.UnexpectedFault.md)| Thrown if an unexpected error occurs while performing the operation.

Show WSDL type definition







Retrieves log collection task information for current logged-in user.

**Privileges**

Privilege | Description
:---|:---
LOG_COLLECTION|  Log collection privilege is required to perform log collection operations.



**Parameters**

 Name | Type | Description
:---|:---|:---
**_this**| [ManagedObjectReference](vmodl.ManagedObjectReference.md)|  A reference to the [LogCollector](vdi.utils.logcollector.LogCollector.md) used to make the method call.



**Return Value**

Type | Description
:---|:---
[LogCollectorTaskInfo[]](vdi.utils.logcollector.LogCollector.LogCollectorTaskInfo.md)| Array of [LogCollectorTaskInfo](vdi.utils.logcollector.LogCollector.LogCollectorTaskInfo.md) \- Log collector task information for current user is returned.



**Faults**

Type | Description
:---|:---
[EntityNotFound](vdi.fault.EntityNotFound.md)| Thrown if any specified entity cannot be found.
[InsufficientPermission](vdi.fault.InsufficientPermission.md)| Thrown if the user does not have sufficient permission to perform the operation.
[InvalidArgument](vdi.fault.InvalidArgument.md)| Thrown if any specified argument is invalid.
[InvalidType](vdi.fault.InvalidType.md)| Thrown if the type of any specified argument is invalid.
[PartialFailureFault](vdi.fault.PartialFailureFault.md)| [^161] [^160]
[UnexpectedFault](vdi.fault.UnexpectedFault.md)| Thrown if an unexpected error occurs while performing the operation.

Show WSDL type definition







Retrieves log collection task information for specified task identifiers. Only the task identifiers owned by the current user are returned.

**Privileges**

Privilege | Description
:---|:---
LOG_COLLECTION|  Log collection privilege is required to perform log collection operations.



**Parameters**

 Name | Type | Description
:---|:---|:---
**_this**| [ManagedObjectReference](vmodl.ManagedObjectReference.md)|  A reference to the [LogCollector](vdi.utils.logcollector.LogCollector.md) used to make the method call.
**logCollectorTaskIdList**| [LogCollectorTaskId[]](vdi.entity.LogCollectorTaskId.md)|  \- A unique task identifier generated from log collect request for monitoring the status.




**Return Value**

Type | Description
:---|:---
[LogCollectorTaskInfo[]](vdi.utils.logcollector.LogCollector.LogCollectorTaskInfo.md)| Array of [LogCollectorTaskInfo](vdi.utils.logcollector.LogCollector.LogCollectorTaskInfo.md)



**Faults**

Type | Description
:---|:---
[EntityNotFound](vdi.fault.EntityNotFound.md)| Thrown if any specified entity cannot be found.
[InsufficientPermission](vdi.fault.InsufficientPermission.md)| Thrown if the user does not have sufficient permission to perform the operation.
[InvalidArgument](vdi.fault.InvalidArgument.md)| Thrown if any specified argument is invalid.
[InvalidType](vdi.fault.InvalidType.md)| Thrown if the type of any specified argument is invalid.
[PartialFailureFault](vdi.fault.PartialFailureFault.md)| [^161] [^160]
[UnexpectedFault](vdi.fault.UnexpectedFault.md)| Thrown if an unexpected error occurs while performing the operation.

Show WSDL type definition







Retrieves all the log collector task information.

**Privileges**

Privilege | Description
:---|:---
ADMINISTRATOR|  Administrator privilege is required along with LOG_COLLECTION privilege to perform list operation.
LOG_COLLECTION|  Log collection privilege is required along with ADMINISTRATOR privilege to perform list operation.



**Parameters**

 Name | Type | Description
:---|:---|:---
**_this**| [ManagedObjectReference](vmodl.ManagedObjectReference.md)|  A reference to the [LogCollector](vdi.utils.logcollector.LogCollector.md) used to make the method call.
**userOrGroupId**| [UserOrGroupId](vdi.entity.UserOrGroupId.md)|  \- Optional field to filter the task information based on the user or group. [^135]





**Return Value**

Type | Description
:---|:---
[LogCollectorTaskInfo[]](vdi.utils.logcollector.LogCollector.LogCollectorTaskInfo.md)| Array of [LogCollectorTaskInfo](vdi.utils.logcollector.LogCollector.LogCollectorTaskInfo.md) [^162] [^163]





**Faults**

Type | Description
:---|:---
[EntityNotFound](vdi.fault.EntityNotFound.md)| Thrown if any specified entity cannot be found.
[InsufficientPermission](vdi.fault.InsufficientPermission.md)| Thrown if the user does not have sufficient permission to perform the operation.
[InvalidArgument](vdi.fault.InvalidArgument.md)| Thrown if any specified argument is invalid.
[InvalidType](vdi.fault.InvalidType.md)| Thrown if the type of any specified argument is invalid.
[LogCollectorFault](vdi.fault.LogCollectorFault.md)|
[UnexpectedFault](vdi.fault.UnexpectedFault.md)| Thrown if an unexpected error occurs while performing the operation.

Show WSDL type definition







Purges the log collection bundle for the provided list of targets.

**Privileges**

Privilege | Description
:---|:---
ADMINISTRATOR|  Administrator privilege is required along with LOG_COLLECTION privilege to perform log collection purge operation.
LOG_COLLECTION|  Log collection privilege is required along with ADMINISTRATOR privilege to perform log collection purge operation.



**Parameters**

 Name | Type | Description
:---|:---|:---
**_this**| [ManagedObjectReference](vmodl.ManagedObjectReference.md)|  A reference to the [LogCollector](vdi.utils.logcollector.LogCollector.md) used to make the method call.
**componentIdentifiers**| [LogCollectorComponentIdentifier[]](vdi.utils.logcollector.LogCollector.LogCollectorComponentIdentifier.md)|




**Return Value**

Type | Description
:---|:---
[LogCollectorTaskInfo[]](vdi.utils.logcollector.LogCollector.LogCollectorTaskInfo.md)| Array of [LogCollectorTaskInfo](vdi.utils.logcollector.LogCollector.LogCollectorTaskInfo.md)



**Faults**

Type | Description
:---|:---
[EntityNotFound](vdi.fault.EntityNotFound.md)| Thrown if any specified entity cannot be found.
[InsufficientPermission](vdi.fault.InsufficientPermission.md)| Thrown if the user does not have sufficient permission to perform the operation.
[InvalidArgument](vdi.fault.InvalidArgument.md)| Thrown if any specified argument is invalid.
[InvalidType](vdi.fault.InvalidType.md)| Thrown if the type of any specified argument is invalid.
[PartialFailureFault](vdi.fault.PartialFailureFault.md)| [^161] [^160]
[UnexpectedFault](vdi.fault.UnexpectedFault.md)| Thrown if an unexpected error occurs while performing the operation.



**Events**

Event | Description
:---|:---
VLSI_LOG_COLLECTION_PURGE_TASK_SUCCESS|  \- Generated for each of the log component type when the log purge request is successfully submitted

Show WSDL type definition







Updates feature specific log level for a component.

**Privileges**

Privilege | Description
:---|:---
LOG_COLLECTION|  Log collection privilege is required to perform log level operations.



**Parameters**

 Name | Type | Description
:---|:---|:---
**_this**| [ManagedObjectReference](vmodl.ManagedObjectReference.md)|  A reference to the [LogCollector](vdi.utils.logcollector.LogCollector.md) used to make the method call.
**logLevelSpec**| [LogLevelSpec](vdi.utils.logcollector.LogCollector.LogLevelSpec.md)|  Log level spec to update new log levels for a component.




**Return Value**

Type | Description
:---|:---
[LogLevelInfo](vdi.utils.logcollector.LogCollector.LogLevelInfo.md)| [LogLevelInfo](vdi.utils.logcollector.LogCollector.LogLevelInfo.md) \- Contains updated feature-wise log level information for a component



**Faults**

Type | Description
:---|:---
[EntityNotFound](vdi.fault.EntityNotFound.md)| Thrown if any specified entity cannot be found.
[InsufficientPermission](vdi.fault.InsufficientPermission.md)| Thrown if the user does not have sufficient permission to perform the operation.
[InvalidArgument](vdi.fault.InvalidArgument.md)| Thrown if any specified argument is invalid.
[InvalidType](vdi.fault.InvalidType.md)| Thrown if the type of any specified argument is invalid.
[LogCollectorFault](vdi.fault.LogCollectorFault.md)| Thrown if the getLogLevels fails for the given component.
[UnexpectedFault](vdi.fault.UnexpectedFault.md)| Thrown if an unexpected error occurs while performing the operation.

Show WSDL type definition












 


[^135]: This parameter need not be set.
[^159]: Contains null for which the request is processed successfully.
[^160]: [LogCollectorFault](vdi.fault.LogCollectorFault.md) for failed ones.
[^161]: Contains array of [LogCollectorTaskInfo](vdi.utils.logcollector.LogCollector.LogCollectorTaskInfo.md) for which the request is processed successfully.
[^162]: All available log collector task information is returned if no parameter used.
[^163]: Log collector task information for specified user returned if parameter used.