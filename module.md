---
title: module
short_desc: module type documentation
tags: api
path: lua_api/module
uuid: d8700912-8312-195f-8886-25587a4606a5
public: true
private: false
---



### Properties

* **savedAuthorid** *any* 

### Functions

function **module.AdminAbsorbModules**()
  return *nil*

function **module.PrepareModuleStats**(fn)
  parameter **fn** *any*
  return *nil*

function **module.QueryModuleIndex**(options)
  parameter **options** *any*
  return *nil*

function **module.CreateDependencySearcher**(dynGuidsAll)
  parameter **dynGuidsAll** *any*
  return *any*

function **module.CreateModule**()
  return *any*

function **module.GetModule**(fullid)
  parameter **fullid** *string*
  return *any*

function **module.GetOurPurchasedModules**()
  return *any*

function **module.GetOurPublishedModules**()
  return *any*

function **module.GetModulesPublishedFromThisGame**()
  return *any*

function **module.DownloadModuleInfo**(options)
  parameter **options** *any*
  return *nil*

function **module.CalculateDownloadSizeInKBytes**(dynGuids)
  parameter **dynGuids** *any*
  return *any*

function **module.GetEligibleDependentModules**(dynModuleid)
  parameter **dynModuleid** *any*
  return *any*

function **module.GetLoadedModules**()
  return *any*

function **module.GetDisabledModules**()
  return *any*

function **module.GetModuleDependencies**(callback)
  parameter **callback** *any*
  return *nil*

function **module.GuidsLoaded**(modulesList, options)
  parameter **modulesList** *any*
  parameter **options** *any*
  return *any*

function **module.GetMonsterEntryChanges**(guid)
  parameter **guid** *string*
  return *any*

function **module.GetObjectTableChanges**(tableName, guid)
  parameter **tableName** *string*
  parameter **guid** *string*
  return *any*

function **module.HasNovelContent**(contentType, key)
  parameter **contentType** *any*
  parameter **key** *any*
  return *any*

function **module.GetNovelContent**(contentType)
  parameter **contentType** *string*
  return *any*

function **module.RemoveNovelContent**(contentType, id)
  parameter **contentType** *string*
  parameter **id** *any*
  return *nil*
