---
title: MapManifestLua
short_desc: MapManifestLua type documentation
tags: api
path: lua_api/MapManifestLua
uuid: 14134d03-1081-9b55-aec7-5f7f3e7c6100
public: true
private: false
---



### Properties

* **id** *string* 
* **valid** *boolean* 
* **mapManifest** *any* 
* **dimensions** *any* 
* **loadingScreenImage** *string* 
* **groundLevel** *any* 
* **description** *any* 
* **floorsWithoutLayers** *any* 
* **floors** *any* 
* **parentFolder** *any* 
* **ord** *number* 

### Functions

function **MapManifestLua:MarkUndo**()
  return *nil*

function **MapManifestLua:Upload**(description)
  parameter **description** *string*
  return *nil*

function **MapManifestLua:Delete**()
  return *nil*

function **MapManifestLua:GetFloorFromLoc**(loc)
  parameter **loc** *any*
  return *any*

function **MapManifestLua:GetLayersForFloor**(parentFloorId)
  parameter **parentFloorId** *any*
  return *any*

function **MapManifestLua:CreateFloor**(options)
  parameter **options** *any*
  return *nil*

function **MapManifestLua:CreatePreviewFloor**(floorBasis)
  parameter **floorBasis** *string*
  return *any*

function **MapManifestLua:DestroyPreviewFloor**(floorInfo)
  parameter **floorInfo** *any*
  return *nil*

function **MapManifestLua:Travel**()
  return *nil*
