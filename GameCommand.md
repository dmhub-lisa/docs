---
title: GameCommand
short_desc: GameCommand type documentation
tags: api
path: lua_api/GameCommand
uuid: 252ac33e-3ecd-895c-b748-16b0357164b1
public: true
private: false
---



### Properties

* **executing** *boolean* 
* **busy** *boolean* 

### Functions

function **GameCommand:AddCommandToGroup**(cmd)
  parameter **cmd** *any*
  return *nil*

function **GameCommand:Execute**(isRedo)
  parameter **isRedo** *boolean?*
  return *nil*

function **GameCommand:Undo**()
  return *nil*
