---
title: code
short_desc: code type documentation
tags: api
path: lua_api/code
uuid: 8ad09456-532e-ca5f-a0c3-103e5ad6f607
public: true
private: false
---



### Properties

* **loadedMods** *any* 
* **loadedModsLocalToGame** *any* 
* **monitorid** *string* 
* **logEvent** *any* 
* **modifyEvent** *any* 

### Functions

function **code.UserEditCodeDevConfig**()
  return *nil*

function **code.GetCodeFromMD5**(md5)
  parameter **md5** *any*
  return *any*

function **code.GetMod**(modid)
  parameter **modid** *string*
  return *any*

function **code.LaunchExternalDiff**(md5a, md5b)
  parameter **md5a** *string*
  parameter **md5b** *string*
  return *nil*

function **code.Diff**(a, b)
  parameter **a** *string*
  parameter **b** *string*
  return *any*

function **code.CanDeleteMod**(modid)
  parameter **modid** *string*
  return *boolean*

function **code.DeleteMod**(modid)
  parameter **modid** *string*
  return *nil*

function **code.CreateMod**()
  return *nil*
