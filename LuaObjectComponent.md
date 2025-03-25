---
title: LuaObjectComponent
short_desc: LuaObjectComponent type documentation
tags: api
path: lua_api/LuaObjectComponent
uuid: 943c8757-f71d-4b58-a749-33819731064b
public: true
private: false
---



### Properties

* **componentType** *string* 
* **commands** *any* 
* **_levelObject** *any* 
* **preview** *boolean* 
* **sheet** *any* 
* **type** *any* 
* **behaviorDescription** *any* 
* **valid** *boolean* 
* **name** *string* 
* **displayPriority** *number* 
* **tooltip** *string* 
* **fields** *any* 
* **disabled** *boolean* 
* **deletable** *boolean* 
* **properties** *any* 
* **objectInstance** *any* 

### Functions

function **LuaObjectComponent:SetProperty**(id, val)
  parameter **id** *string*
  parameter **val** *any*
  return *nil*

function **LuaObjectComponent:Execute**(commandDescription)
  parameter **commandDescription** *any*
  return *nil*

function **LuaObjectComponent:ThinkEdit**()
  return *nil*

function **LuaObjectComponent:UpdateBlueprint**(newAsset)
  parameter **newAsset** *boolean?*
  return *nil*

function **LuaObjectComponent:GetFieldDisplayInfo**(obj, fieldName)
  parameter **obj** *any*
  parameter **fieldName** *string*
  return *any*

function **LuaObjectComponent:BeginChanges**()
  return *nil*

function **LuaObjectComponent:CompleteChanges**(description)
  parameter **description** *string*
  return *nil*

function **LuaObjectComponent:DestroyObject**()
  return *nil*

function **LuaObjectComponent:RecordUndo**()
  return *nil*

function **LuaObjectComponent:Upload**(cmdgroupid)
  parameter **cmdgroupid** *string?*
  return *nil*

function **LuaObjectComponent:SetAndUploadProperties**(dict)
  parameter **dict** *any*
  return *nil*

function **LuaObjectComponent:CreateCustomEditor**()
  return *any*
