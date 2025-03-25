---
title: tutorial
short_desc: tutorial type documentation
tags: api
path: lua_api/tutorial
uuid: 0e0330fe-2e10-8f5f-ab72-edd523758d54
public: true
private: false
---



### Properties

* **text** *any* 
* **tutorialName** *any* 
* **eventSource** *any* 

### Functions

function **tutorial.SetTutorial**(tutorial)
  parameter **tutorial** *any*
  return *nil*

function **tutorial.ClearTutorial**()
  return *nil*

function **tutorial.CompleteTutorial**()
  return *nil*

function **tutorial.IsTutorialComplete**(name)
  parameter **name** *string*
  return *boolean*

function **tutorial.MarkTutorialComplete**(name)
  parameter **name** *string*
  return *nil*
