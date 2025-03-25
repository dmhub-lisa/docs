---
title: GameAsset
short_desc: GameAsset type documentation
tags: api
path: lua_api/GameAsset
uuid: 7f231732-472a-785f-be48-ed99a6f841be
public: true
private: false
---



### Properties

* **cachePath** *string* 
* **sizeInKBytes** *number* 

### Functions

function **GameAsset:ValidationCheck**(objtype, guid)
  parameter **objtype** *string*
  parameter **guid** *string*
  return *boolean*

function **GameAsset:MatchesSearch**(searchLowercase)
  parameter **searchLowercase** *string*
  return *boolean*

function **GameAsset:OnLoad**()
  return *nil*
