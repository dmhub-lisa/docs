---
title: LuaSheetMapImport
short_desc: LuaSheetMapImport type documentation
tags: api
path: lua_api/LuaSheetMapImport
uuid: c982d9fb-bbd2-2758-8f51-5deea78687eb
public: true
private: false
---

 : [:Panel](/lua_api/LuaSheetMapImport)

### Properties

* **errorMessage** *any* 
* **path** *any* 
* **paths** *any* 
* **pathIndex** *any* 
* **instructionsText** *any* 
* **haveConfirm** *any* 
* **haveNext** *any* 
* **havePrevious** *any* 
* **tileDim** *any* 
* **error** *any* 
* **zoom** *any* 
* **tileType** *any* 
* **lockDimensions** *boolean* 
* **tileScaling** *number* 

### Functions

function **LuaSheetMapImport:Next**()
  return *nil*

function **LuaSheetMapImport:Previous**()
  return *nil*

function **LuaSheetMapImport:Confirm**(callback)
  parameter **callback** *any*
  return *nil*

function **LuaSheetMapImport:SetWidth**(w)
  parameter **w** *any*
  return *nil*

function **LuaSheetMapImport:SetHeight**(h)
  parameter **h** *any*
  return *nil*

function **LuaSheetMapImport:CreateGridless**()
  return *nil*

function **LuaSheetMapImport:ClearMarkers**()
  return *nil*
