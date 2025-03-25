---
title: SheetHud
short_desc: SheetHud type documentation
tags: api
path: lua_api/SheetHud
uuid: 2054616e-1fe3-1055-a6c1-394858d9dbc2
public: true
private: false
---



### Properties

* **selectedTokenOverride** *any* 
* **selectedToken** *any* 
* **selectedOrPrimaryTokens** *any* 
* **tokens** *any* 
* **initiativeQueue** *any* 

### Functions

function **SheetHud:PushSelectedTokenOverride**(token)
  parameter **token** *any*
  return *nil*

function **SheetHud:PopSelectedTokenOverride**()
  return *nil*

function **SheetHud.TokensInShape**(area)
  parameter **area** *any*
  return *any*

function **SheetHud.GetToken**(tokenid)
  parameter **tokenid** *any*
  return *any*

function **SheetHud.UploadInitiative**()
  return *nil*
