---
title: GameRules
short_desc: GameRules type documentation
tags: api
path: lua_api/GameRules
uuid: 8a49b1c1-2ee1-2552-b358-55dba7c4d10c
public: true
private: false
---



### Properties

* **CreatureSizes** *any* 

### Functions

function **GameRules.GetSizeInfo**(index)
  parameter **index** *number*
  return *any*

function **GameRules.NormalizeSizeIndex**(index)
  parameter **index** *number*
  return *number*

function **GameRules.StringToCreatureSizeIndex**(name)
  parameter **name** *string*
  return *number*

function **GameRules.CreatureSizeIndexToString**(index)
  parameter **index** *number*
  return *string*
