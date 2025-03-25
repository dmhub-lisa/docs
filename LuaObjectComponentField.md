---
title: LuaObjectComponentField
short_desc: LuaObjectComponentField type documentation
tags: api
path: lua_api/LuaObjectComponentField
uuid: 2b2abca9-60c3-6f5a-8d3b-2a3b4926cf3a
public: true
private: false
---



### Properties

* **currentValue** *any* 
* **count** *number* 
* **fieldType** *string* 
* **id** *string* 
* **prettyName** *string* 
* **arguments** *any* 
* **canUpload** *boolean* 

### Functions

function **LuaObjectComponentField:GetEditingInfo**()
  return *any*

function **LuaObjectComponentField:GetValue**(index)
  parameter **index** *number*
  return *any*

function **LuaObjectComponentField:SetValue**(val, index)
  parameter **val** *any*
  parameter **index** *number*
  return *nil*

function **LuaObjectComponentField:Append**()
  return *nil*

function **LuaObjectComponentField:Remove**(index)
  parameter **index** *number*
  return *nil*

function **LuaObjectComponentField:MarkUndoPoint**()
  return *nil*

function **LuaObjectComponentField:Upload**(cmdgroupid)
  parameter **cmdgroupid** *string?*
  return *nil*
