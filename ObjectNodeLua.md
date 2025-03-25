---
title: ObjectNodeLua
short_desc: ObjectNodeLua type documentation
tags: api
path: lua_api/ObjectNodeLua
uuid: d0c00f33-3af5-e753-9015-637e7c57d36b
public: true
private: false
---

 : [:AssetNodeBaseLua](/lua_api/ObjectNodeLua)

### Properties

* **previewType** *any* 
* **keywords** *any* 
* **isfolder** *any* 
* **image** *any* 
* **imageId** *any* 
* **thumbnailId** *any* 
* **scale** *any* 
* **components** *any* 
* **hue** *number* 
* **brightness** *number* 
* **saturation** *number* 

### Functions

function **ObjectNodeLua:Restore**(json)
Restores this from json.
  parameter **json** *string*
  return *nil*

function **ObjectNodeLua:Upload**()
  return *nil*

function **ObjectNodeLua:Delete**()
  return *nil*

function **ObjectNodeLua:Duplicate**()
  return *nil*

function **ObjectNodeLua:UpdateObjectInstances**()
  return *nil*

function **ObjectNodeLua:AddComponent**(componentName)
  parameter **componentName** *string*
  return *any*

function **ObjectNodeLua.BuildObjectComponentByName**(componentName)
  parameter **componentName** *string*
  return *any*

function **ObjectNodeLua:IsValidComponentJson**(doc)
  parameter **doc** *any*
  return *any*

function **ObjectNodeLua:ConstructComponent**(doc)
  parameter **doc** *any*
  return *any*

function **ObjectNodeLua:ComponentToJson**(key)
  parameter **key** *string*
  return *any*

function **ObjectNodeLua:RemoveComponent**(componentNameOrKey)
  parameter **componentNameOrKey** *string*
  return *nil*
