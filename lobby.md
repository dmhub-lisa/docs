---
title: lobby
short_desc: lobby type documentation
tags: api
path: lua_api/lobby
uuid: 76c05d4b-b9e7-2251-b3c8-9121a9710fc7
public: true
private: false
---



### Properties

* **maxGameDetailsLength** *any* 
* **maxGameTitleLength** *any* 
* **maxGamePasswordLength** *any* 
* **gamesRevision** *any* 
* **games** *any* 
* **createdGameId** *any* 
* **createdGameIdAge** *any* 
* **deletedGameId** *any* 

### Functions

function **lobby:CreateGame**()
  return *nil*

function **lobby:EnterGame**(gameid)
  parameter **gameid** *string*
  return *nil*

function **lobby:LookupGame**(gameid, callback)
  parameter **gameid** *any*
  parameter **callback** *any*
  return *nil*

function **lobby:JoinGame**(gameid)
  parameter **gameid** *string*
  return *nil*
