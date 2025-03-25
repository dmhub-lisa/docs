---
title: ModuleLua
short_desc: ModuleLua type documentation
tags: api
path: lua_api/ModuleLua
uuid: c8af47de-3c53-1559-bb99-fbdde2ff409b
public: true
private: false
---



### Properties

* **idvalid** *boolean* 
* **fullid** *any* 
* **authorid** *string* 
* **moduleid** *string* 
* **name** *string* 
* **details** *string* 
* **keywords** *any* 
* **keywordsAsJoinedString** *any* 
* **coverart** *any* 
* **owned** *boolean* 
* **premium** *boolean* 
* **published** *boolean* 
* **dmhubCanUse** *boolean* 
* **publishingProperties** *any* 
* **contentSummary** *any* 
* **isdisabled** *boolean* 
* **ourModule** *boolean* 
* **publishedFromThisGame** *any* 
* **loadedVersion** *any* 
* **installedVersion** *any* 
* **latestVersion** *any* 
* **installationBandwidthInKBytes** *any* 
* **versions** *any* 
* **cachedStats** *any* 
* **vote** *number* 

### Functions

function **ModuleLua:IsModuleIdValid**(id)
  parameter **id** *string*
  return *boolean*

function **ModuleLua:IsAuthorIdValid**(id)
  parameter **id** *string*
  return *boolean*

function **ModuleLua:Upload**(options)
  parameter **options** *any*
  return *nil*

function **ModuleLua:ReserveAuthorID**(options)
  parameter **options** *any*
  return *nil*

function **ModuleLua:CheckAuthorIDAvailable**(callback)
  parameter **callback** *any*
  return *nil*

function **ModuleLua:CheckModuleIDAvailable**(options)
  parameter **options** *any*
  return *nil*

function **ModuleLua:UploadModuleVersion**(options)
  parameter **options** *any*
  return *nil*

function **ModuleLua:UploadModulePublishProperties**(properties)
  parameter **properties** *any*
  return *nil*

function **ModuleLua:Install**(options)
  parameter **options** *any*
  return *nil*

function **ModuleLua:Uninstall**(options)
  parameter **options** *any*
  return *nil*

function **ModuleLua:SetDisabled**(disabled)
  parameter **disabled** *boolean*
  return *nil*

function **ModuleLua:QueryStats**(fn)
  parameter **fn** *any*
  return *nil*
