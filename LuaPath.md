---
title: LuaPath
short_desc: LuaPath type documentation
tags: api
path: lua_api/LuaPath
uuid: 4f474c50-64e2-875e-895e-1356e9f638a1
public: true
private: false
---



### Properties

* **forced** *boolean* 
* **forcedDest** *nil|Loc* 
* **forcedMovementTotalDistance** *number* 
* **collisionSpeed** *number* 
* **mount** *any* 
* **waterSteps** *any* 
* **difficultSteps** *any* 
* **squeezeSteps** *any* 
* **numDiagonals** *any* 
* **cost** *any* 
* **numSteps** *any* 
* **destinationPosition** *any* 
* **destination** *any* 
* **origin** *any* 
* **steps** *Loc[]* 

### Functions

function **LuaPath:CalculateHazards**(tok)
  parametertok CharacterToken
  returnnil|{type: 'damage', damageAmount: number, damageType: string, aura: AuraInstance}[]
