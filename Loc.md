---
title: Loc
short_desc: Loc type documentation
tags: api
path: lua_api/Loc
uuid: 2eaf67ec-e076-9b58-8aea-a007486d17cf
public: true
private: false
---



### Properties

* **west** *any* 
* **east** *any* 
* **north** *any* 
* **south** *any* 
* **x** *any* 
* **y** *any* 
* **floor** *any* 
* **altitude** *any* 
* **xyfloorOnly** *any* 
* **xyOnly** *any* 
* **isOnMap** *any* 
* **valid** *any* 
* **point2** *any* 
* **point3** *any* 
* **str** *string* 

### Functions

function **Loc:Deserialize**(dict)
  parameter **dict** *any*
  return *nil*

function **Loc:Equals**(other)
  parameter **other** *any*
  return *boolean*

function **Loc:DistanceInTiles**(other)
  parameter **other** *any*
  return *number*

function **Loc:DistanceInFeet**(other)
  parameter **other** *any*
  return *number*

function **Loc:dir**(x, y)
  parameter **x** *number*
  parameter **y** *number*
  return *any*

function **Loc:FloorDifference**(loc)
  parameter **loc** *any*
  return *number*

function **Loc:LocsInRadius**(radius)
  parameter **radius** *number*
  return *any*
