---
layout: page
title: Data Object - GlobalApplicationEntitlementBase
hide:
#  - navigation
  - toc
---





Java Class
> `com.omnissa.vdi.vlsi.binding.vdi.federation.GlobalApplicationEntitlement.GlobalApplicationEntitlementBase`

Property of
> [GlobalApplicationEntitlementInfo](vdi.federation.GlobalApplicationEntitlement.GlobalApplicationEntitlementInfo.md#field_detail)

Parameter to
> [GlobalApplicationEntitlement_Create](vdi.federation.GlobalApplicationEntitlement.md#create)

See also
> [GlobalAccessGroupId](vdi.entity.GlobalAccessGroupId.md), [GlobalApplicationEntitlementId](vdi.entity.GlobalApplicationEntitlementId.md)

Since
> Horizon View 6.2


## Data Object Description

Parameters to create a Global Application Entitlement.

## Data Object Properties

 Name | Type | Description
:---|:---:|:---
**displayName**|  xsd:string|  The display name is the unique name used to identify the Global Application Entitlement. [^128]
**aliasName**|  xsd:string|  The alias name is the name that users will see when they connect using Horizon View Client. If the alias name is left blank, while creating or updating the Global Application Entitlement alias name value will be same as display name.  **_Since_** Horizon 8.0 [^1] [^128]
**description**|  xsd:string|  Description of Global Application Entitlement. [^1] [^13]
**scope**|  xsd:string|  Scope for this global application entitlement. Visibility and Placement policies are defined by this value. [^129] [^1]<br>* This property will be one of:<br><table><thead><tr><th>Value</th><th>Description</th></tr></thead><tbody><tr><td>"LOCAL"</td><td>Local Policy: Local pod will be used for this policy. If this policy is for visibility, search for existing session will happen only in local pod. If this policy is for placement, session will always be placed on local pod.</td></tr><tr><td>"SITE"</td><td>Site Policy: Site will be used for this policy. If this policy is for visibility, search for existing session will happen only from site. If this policy is for placement, session will be placed on site.</td></tr><tr><td>"ANY"</td><td>Any Policy: Any pod can be used for this action. If this policy is for visibility, search for existing session will span all pods in LMV set. If this policy is for placement, session can be placed on any pod in LMV set.</td></tr></tbody></table>
**fromHome**|  xsd:boolean|  This value defines the starting location for resource placement and search. When true, a pod in the user's home site is used to start the search. When false, the current site is used.
**requireHomeSite**|  xsd:boolean|  This value determines whether we fail if a home site isn't defined for this Global Application Entitlement.
**multipleSessionAutoClean**|  xsd:boolean|  This value is used to determine if automatic session clean up is enabled.
**enabled**|  xsd:boolean|  If this Global Application Entitlement is enabled.
**supportedDisplayProtocols**|  xsd:string[]|  The set of supported display protocols for the Global Application Entitlement. Farms support PCOIP, RDP and BLAST. This setting must be a subset of the farm settings. Clients connecting through this Global Application Entitlement that are allowed to select their protocol will see these display protocol options. [^131] [^14] [^2] <br>* This property will be one of:<br><table><tr><th>Value</th><th>Description</th></tr><tr><td>"PCOIP"</td><td>PC over IP.</td></tr><tr><td>"BLAST"</td><td>BLAST.</td></tr></table>
**defaultDisplayProtocol**|  xsd:string|  The default display protocol for the Global Application Entitlement. Must be a protocol in the supportedDisplayProtocols list. [^111] [^1] <br>* This property will be one of:<br><table><tr><th>Value</th><th>Description</th></tr><tr><td>"PCOIP"</td><td>PC over IP.</td></tr><tr><td>"BLAST"</td><td>BLAST.</td></tr></table>
**allowUsersToChooseProtocol**|  xsd:boolean|  Whether the users can choose the protocol to be used. If this Application's Farm's [allowDisplayProtocolOverride](vdi.resources.Farm.DisplayProtocolSettings.md#allowDisplayProtocolOverride) is set to false, then [defaultDisplayProtocol](vdi.federation.GlobalApplicationEntitlement.GlobalApplicationEntitlementBase.md#defaultDisplayProtocol) must match that [defaultDisplayProtocol](vdi.resources.Farm.DisplayProtocolSettings.md#defaultDisplayProtocol). [^6] [^2]
**enableHTMLAccess**|  xsd:boolean| **Deprecated.**_This property is no longer in use for Horizon Components. It is always set to true._ HTML Access, enabled by VMware Blast technology, allows users to connect to View machines from Web browsers. View Client software does not have to be installed on the client devices. To enable HTML Access, you must install the HTML Machine Access feature pack. If set to true, the farms of applications that are associated with this Global Application Entitlement must also have HTML Access enabled with [enableHTMLAccess](vdi.resources.Farm.DisplayProtocolSettings.md#enableHTMLAccess) Also, Blast must be configured as a supported protocol in [supportedDisplayProtocols](vdi.federation.GlobalApplicationEntitlement.GlobalApplicationEntitlementBase.md#supportedDisplayProtocols). [^6] [^1]
**connectionServerRestrictions**|  xsd:string[]|  Connection server restrictions. This is a list of tags that access to the entitlement is restricted to. No list means that the entitlement can be accessed from any connection server.  **_Since_** Horizon 7.1 [^1]
**enablePreLaunch**|  xsd:boolean|  This global application entitlement can be pre-launched if value is true.  **_Since_** Horizon 7.2 [^5] [^1]
**categoryFolderName**|  xsd:string|  Name of the category folder in the user's OS containing a shortcut to the entitlement. Unset if the entitlement does not belong to a category.  **_Since_** Horizon 7.3 [^1] [^132]
**clientRestrictions**|  xsd:boolean|  Client restrictions to be applied to Global Application Entitlement. Currently it is valid for RDSH pools.  **_Since_** Horizon 7.3 [^5] [^1]
**shortcutLocations**|  xsd:string[]|  Locations of the category folder in the user's OS containing a shortcut to the desktop. The value must be set if [categoryFolderName](vdi.federation.GlobalApplicationEntitlement.GlobalApplicationEntitlementBase.md#categoryFolderName) is provided.  **_Since_** Horizon 7.5 [^1]
**multiSessionMode**|  xsd:string|  Multi-session mode for this entitlement. A global application entitlement launched in multi-session mode does not support reconnect behavior when user logs in from a different client instance. [enablePreLaunch](vdi.federation.GlobalApplicationEntitlement.GlobalApplicationEntitlementBase.md#enablePreLaunch) can be set to true only if multiSessionMode is disabled.  **_Since_** Horizon 7.7 [^17] [^1] <br>* This property will be one of:<br><table><tr><th>Value</th><th>Description</th></tr><tr><td>"DISABLED"</td><td>Multi-session is not supported for this entitlement.</td></tr><tr><td>"ENABLED_DEFAULT_OFF"</td><td>Multi-session is supported for this entitlement but is disabled by default. The client would need to explicitly request multi-session launch, if wanted. If a legacy client is used, this will always result in a single-session session launch.</td></tr><tr><td>"ENABLED_DEFAULT_ON"</td><td>Multi-session mode is supported for this entitlement and is enabled by default. The client can request explicitly for single-session launch, if wanted. If a legacy client is used, this will always result in a multi-session session launch.</td></tr><tr><td>"ENABLED_ENFORCED"</td><td>Multi-session is supported for this entitlement and it is enforced. The client can not select to launch this entitlement in single-session mode.</td></tr></table>
**backupGAE**| [GlobalApplicationEntitlementId](vdi.entity.GlobalApplicationEntitlementId.md)|  Indicates the Global Application Entitlement that can be used as backup for this Global Application Entitlement.  **_Since_** Horizon 7.11 [^1]
**globalAccessGroupId**| [GlobalAccessGroupId](vdi.entity.GlobalAccessGroupId.md)|  Global access groups can organize the global application entitlements in your organization. They can also be used for delegated administration.  **_Since_** Horizon 8.2 [^1]


 


[^1]: This property need not be set.
[^2]: This property cannot be updated.
[^5]: This property has a default value of false.
[^6]: This property has a default value of true.
[^13]: This property has a maximum length of 1024 characters.
[^14]: This property is an unordered array of unique values.
[^17]: This property has a default value of 'DISABLED'.
[^111]: This property has a default value of 'PCOIP'.
[^128]: This property has a maximum length of 64 characters.
[^129]: This property has a default value of 'ANY'.
[^131]: This property has a default value of ['PCOIP', 'BLAST'].
[^132]: This property defines valid folder names with a max length of 64 characters and up to 4 subdirectory levels. The subdirectories can be specified using a backslash, e.g. (dir1\dir2\dir3\dir4). Folder names can't start or end with a backslash nor can there be 2 or more backslashes together. Combinations such as (\dir1, dir1\dir2\, dir1\\\\dir2, dir1\\\\\\dir2) are invalid. The windows reserved keywords (CON, PRN, NUL, AUX, COM1 - COM9, LPT1 - LPT9 etc.) are not allowed in subdirectory names.