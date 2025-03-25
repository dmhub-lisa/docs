---
title: MapFloorLua
short_desc: MapFloorLua type documentation
tags: api
path: lua_api/MapFloorLua
uuid: a7ed8230-177e-a751-8a69-f213e8c4c209
public: true
private: false
---



### Properties

* **isPrimaryLayerOnFloor** *boolean* 
* **parentFloor** *any* 
* **actualFloor** *any* 
* **preview** *boolean* 
* **valid** *boolean* 
* **mapFloor** *any* 
* **description** *any* 
* **objects** *any* 
* **layerDescription** *any* 
* **invisible** *any* 
* **floorInvisible** *any* 
* **locked** *any* 
* **opacity** *any* 
* **opacityNoUpload** *any* 
* **floorOpacity** *any* 
* **floorOpacityNoUpload** *any* 
* **floorHeightInTiles** *any* 
* **shadowCasting** *any* 
* **renderOrder** *any* 
* **shareLighting** *any* 
* **shareVision** *any* 
* **roof** *any* 
* **roofShowWhenInside** *any* 
* **visionMultiplierNoUpload** *any* 
* **visionMultiplier** *any* 
* **roofVisionExclusion** *any* 
* **roofVisionExclusionNoUpload** *any* 
* **roofMinimumOpacity** *any* 
* **roofMinimumOpacityNoUpload** *any* 
* **roofVisionExclusionFade** *any* 
* **roofVisionExclusionFadeNoUpload** *any* 
* **charactersOnFloor** *any* 
* **playerCharactersOnFloor** *any* 
* **playerCharactersOnLayer** *any* 

### Functions

function **MapFloorLua:AdjustParallaxPositionOnGround**(x, y)
  parameter **x** *any*
  parameter **y** *any*
  return *any*

function **MapFloorLua:HasObject**(keyid)
  parameter **keyid** *string*
  return *boolean*

function **MapFloorLua:GetObject**(keyid)
  parameter **keyid** *string*
  return *any*

function **MapFloorLua:CreateObjectCopy**(luaObjectInstance)
  parameter **luaObjectInstance** *any*
  return *any*

function **MapFloorLua:CreateObject**(obj)
  parameter **obj** *any*
  return *any*

function **MapFloorLua:CreateLocalObjectFromBlueprint**(options)
  parameter **options** *any*
  return *any*

function **MapFloorLua:GetNumberOfProjectiles**(tokenid)
  parameter **tokenid** *string*
  return *any*

function **MapFloorLua:GetProjectiles**(tokenid)
  parameter **tokenid** *string*
  return *any*

function **MapFloorLua:SpawnObjectLocal**(objectid)
  parameter **objectid** *any*
  return *any*

function **MapFloorLua:ExecutePolygonOperation**(options)
  parameter **options** *any*
  return *nil*
