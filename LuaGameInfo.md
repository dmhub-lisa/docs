---
title: LuaGameInfo
short_desc: LuaGameInfo type documentation
tags: api
path: lua_api/LuaGameInfo
uuid: ec2b3130-3727-9f5c-9abd-4b340408b1e6
public: true
private: false
---



### Properties

* **gameSystem** *any* 
* **description** *any* 
* **descriptionDetails** *any* 
* **password** *any* 
* **coverart** *any* 
* **owner** *any* 
* **ownerDisplayName** *any* 
* **dm** *any* 
* **players** *any* 
* **deleted** *any* 
* **timePlayed** *any* 
* **playerSummary** *any* 
* **characterAppearance** *any* 

### Functions

function **LuaGameInfo:MatchesSearch**(searchString)
  parameter **searchString** *string*
  return *boolean*

function **LuaGameInfo:Leave**()
  return *nil*

function **LuaGameInfo:Delete**()
  return *nil*

function **LuaGameInfo:Undelete**()
  return *nil*

function **LuaGameInfo:IsDM**(s)
  parameter **s** *any*
  return *boolean*

function **LuaGameInfo:IsOwner**(s)
  parameter **s** *any*
  return *boolean*

function **LuaGameInfo.GetLocalTimePlayed**(gameid)
  parameter **gameid** *string*
  return *number*

function **LuaGameInfo.SetLocalTimePlayed**(gameid, t)
  parameter **gameid** *string*
  parameter **t** *number*
  return *nil*

function **LuaGameInfo:UploadCoverArt**(options)
  parameter **options** *any*
  return *any*
