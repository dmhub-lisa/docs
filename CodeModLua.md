---
title: CodeModLua
short_desc: CodeModLua type documentation
tags: api
path: lua_api/CodeModLua
uuid: aa13cd51-63f9-c55f-8bfc-6c0f45ed4403
public: true
private: false
---



### Properties

* **dependencies** *any* 
* **valid** *boolean* 
* **canWrite** *boolean* 
* **name** *string* 
* **description** *string* 
* **resources** *any* 
* **isowner** *boolean* 
* **canedit** *boolean* 
* **files** *any* 
* **patches** *any* 
* **changelists** *any* 
* **checkedout** *boolean* 
* **filesThatMayRequireMerge** *nil|CodeModFileLua[]* 
* **localChangeEvent** *any* 
* **hasLocalChanges** *boolean* 

### Functions

function **CodeModLua:AddResource**(p)
  parameter **p** *any*
  return *nil*

function **CodeModLua:ReorderFiles**(a, b)
  parameter **a** *number*
  parameter **b** *number*
  return *nil*

function **CodeModLua:AddFile**()
  return *nil*

function **CodeModLua:Upload**()
  return *nil*

function **CodeModLua:RepairLocal**()
  return *nil*

function **CodeModLua:ImportLocal**()
  return *nil*

function **CodeModLua:DeleteLocalFiles**()
  return *nil*

function **CodeModLua:OpenFile**(file)
  parameter **file** *any*
  return *nil*

function **CodeModLua:GetFileMergeInfo**(file)
  parameter **file** *any*
  return *any*

function **CodeModLua:SaveMerged**(file)
  parameter **file** *any*
  return *boolean*

function **CodeModLua:OpenLocal**()
  return *nil*

function **CodeModLua:CommitChanges**(comment, engineVersion, oncomplete)
  parameter **comment** *string*
  parameter **engineVersion** *string*
  parameter **oncomplete** *any*
  return *string*

function **CodeModLua:SubmitPatch**(comment, engineVersion)
  parameter **comment** *string*
  parameter **engineVersion** *string*
  return *string*

function **CodeModLua:CheckOutPatch**(patchid, callback)
  parameter **patchid** *string*
  parameter **callback** *any*
  return *nil*
