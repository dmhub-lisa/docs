---
title: BrushAssetLua
short_desc: BrushAssetLua type documentation
tags: api
path: lua_api/BrushAssetLua
uuid: 707d10f2-83ee-9a5d-9f50-83ad012f33b3
public: true
private: false
---



### Properties

* **hidden** *boolean* 
* **tipAsset** *string* 
* **blend** *string* 
* **tipRotation** *string* 
* **textureAsset** *string* 
* **textureScale** *number* 
* **opacity** *number* 
* **radius** *number* 
* **fadeRadius** *number* 
* **description** *string* 
* **ord** *any* 

### Functions

function **BrushAssetLua:GetParameter**(fieldName)
  parameter **fieldName** *string*
  return *any*

function **BrushAssetLua:SetParameter**(fieldName, info)
  parameter **fieldName** *string*
  parameter **info** *any*
  return *nil*

function **BrushAssetLua:GetDisplayField**(fieldName)
  parameter **fieldName** *string*
  return *boolean*

function **BrushAssetLua:SetDisplayField**(fieldName, value)
  parameter **fieldName** *string*
  parameter **value** *boolean*
  return *nil*

function **BrushAssetLua:Upload**()
  return *nil*
