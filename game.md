---
title: game
short_desc: game type documentation
tags: api
path: lua_api/game
uuid: b7caa56c-707e-785c-bb4c-14b3d3bf26ba
public: true
private: false
---



### Properties

* **currentMap** *any* 
* **currentMapId** *any* 
* **currentFloor** *any* 
* **currentFloorId** *any* 
* **coverart** *string* 
* **rootMapFolder** *any* 
* **maps** *any* 
* **mapFolders** *any* 

### Functions

function **game.GetFloor**(floorid)
  parameter **floorid** *any*
  return *any*

function **game.DeleteFloor**(luaFloorid)
  parameter **luaFloorid** *any*
  return *nil*

function **game.PrepareDeleteFloor**(floorid, evacuationFloor, patch, unpatch)
  parameter **floorid** *string*
  parameter **evacuationFloor** *any*
  parameter **patch** *any*
  parameter **unpatch** *any*
  return *nil*

function **game.MergeFloors**(floorid, srcid)
  parameter **floorid** *any*
  parameter **srcid** *any*
  return *any*

function **game.PrepareMergeFloors**(groupid, floorid, srcid, patch, unpatch)
  parameter **groupid** *string*
  parameter **floorid** *string*
  parameter **srcid** *string*
  parameter **patch** *any*
  parameter **unpatch** *any*
  return *string*

function **game.ChangeMap**(map, floor)
  parameter **map** *any*
  parameter **floor** *any*
  return *nil*

function **game.FloorIsAboveGround**(floor)
  parameter **floor** *any*
  return *boolean*

function **game.Refresh**(options)
  parameter **options** *any*
  return *nil*

function **game.CreateCharacter**(chartype, subtype)
  parameter **chartype** *any*
  parameter **subtype** *any*
  return *any*

function **game.DeleteCharacters**(charids)
  parameter **charids** *any*
  return *nil*

function **game.LookupObject**(floorid, objectid)
  parameter **floorid** *string*
  parameter **objectid** *string*
  return *any*

function **game.GetObjectsWithAffinityToCharacter**(charid)
  parameter **charid** *string*
  return *any*

function **game.GetAurasAtLoc**(loc)
  parameter **loc** *any*
  return *any*

function **game.GetCharacterById**(id)
  parameter **id** *any*
  return *any*

function **game.GetGameGlobalCharacters**()
  return *any*

function **game.GetTokensAtLoc**(loc)
  parameter **loc** *any*
  return *any*

function **game.UnsummonTokens**(tokenidList)
  parameter **tokenidList** *any*
  return *nil*

function **game.SpawnTokenFromBestiaryLocally**(id, loc)
  parameter **id** *string*
  parameter **loc** *any*
  return *any*

function **game.UpdateCharacterTokens**()
  return *nil*

function **game.GetMap**(id)
  parameter **id** *string*
  return *any*

function **game.CreateMapFolder**()
  return *nil*

function **game.CreateMap**(options)
  parameter **options** *any*
  return *string*

function **game.DuplicateMap**(mapid, oncomplete)
  parameter **mapid** *string*
  parameter **oncomplete** *any*
  return *nil*
