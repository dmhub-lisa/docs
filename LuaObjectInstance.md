---
title: LuaObjectInstance
short_desc: LuaObjectInstance type documentation
tags: api
path: lua_api/LuaObjectInstance
uuid: 076cc113-5d3f-0756-bf69-78b4f77e306d
public: true
private: false
---



### Properties

* **id** *string* 
* **imageid** *string* 
* **assetid** *string* 
* **parentid** *string* 
* **childids** *any* 
* **artist** *string* 
* **editingInfo** *any* 
* **x** *number* 
* **y** *number* 
* **rotation** *number* 
* **scale** *number* 
* **description** *any* 
* **zorder** *number* 
* **editorFocus** *boolean* 
* **editorSelection** *boolean* 
* **childEditorSelection** *boolean* 
* **childEditorFocus** *boolean* 
* **locked** *any* 
* **attachedRulesObjects** *any* 
* **area** *any* 
* **valid** *boolean* 
* **components** *any* 
* **path** *string* 

### Functions

function **LuaObjectInstance:AddComponentFromJson**(id, json)
  parameter **id** *any*
  parameter **json** *any*
  return *nil*

function **LuaObjectInstance:GetComponent**(description)
  parameter **description** *string*
  return *any*

function **LuaObjectInstance:AddComponent**(componentName)
  parameter **componentName** *string*
  return *any*

function **LuaObjectInstance.BuildObjectComponentByName**(componentName)
  parameter **componentName** *string*
  return *any*

function **LuaObjectInstance:IsValidComponentJson**(doc)
  parameter **doc** *any*
  return *any*

function **LuaObjectInstance:ConstructComponent**(doc)
  parameter **doc** *any*
  return *any*

function **LuaObjectInstance:ComponentToJson**(key)
  parameter **key** *string*
  return *any*

function **LuaObjectInstance:RemoveComponent**(key)
  parameter **key** *string*
  return *nil*

function **LuaObjectInstance:MarkUndo**()
  return *nil*

function **LuaObjectInstance:Upload**(cmdgroupid)
  parameter **cmdgroupid** *string?*
  return *nil*

function **LuaObjectInstance:SetAndUploadZOrder**(zorder)
  parameter **zorder** *number*
  return *nil*

function **LuaObjectInstance:SetAndUploadPos**(x, y)
  parameter **x** *number*
  parameter **y** *number*
  return *nil*

function **LuaObjectInstance:Destroy**()
  return *nil*

function **LuaObjectInstance:DestroyWithBehavior**(behavior)
  parameter **behavior** *any*
  return *nil*
