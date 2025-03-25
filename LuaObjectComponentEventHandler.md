---
title: LuaObjectComponentEventHandler
short_desc: LuaObjectComponentEventHandler type documentation
tags: api
path: lua_api/LuaObjectComponentEventHandler
uuid: 88c6f3aa-bd4e-9e59-9de7-c833c531662d
public: true
private: false
---

 : [:LuaObjectComponent](/lua_api/LuaObjectComponentEventHandler)


### Functions

function **LuaObjectComponentEventHandler:GetPossibleEvents**()
  return *any*

function **LuaObjectComponentEventHandler:GetEventEntry**(eventid)
  parameter **eventid** *string*
  return *any*

function **LuaObjectComponentEventHandler:SetEventEntry**(eventid, handled)
  parameter **eventid** *string*
  parameter **handled** *boolean*
  return *nil*

function **LuaObjectComponentEventHandler:TriggerEvent**(eventid)
  parameter **eventid** *string*
  return *nil*
