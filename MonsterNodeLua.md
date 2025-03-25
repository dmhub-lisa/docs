---
title: MonsterNodeLua
short_desc: MonsterNodeLua type documentation
tags: api
path: lua_api/MonsterNodeLua
uuid: 44cdf862-2e42-b557-bc4a-746e30d44b66
public: true
private: false
---



### Properties

* **hidden** *boolean* (Read-only) true if the entry has been 'hidden' in this game (i.e. deleted, but can be undeleted)
* **ord** *number* The ordering of the node, controls whether it is displayed before or after its siblings.
* **description** *string* 
* **monster** *nil|MonsterAssetLua* (Read-only) Get the monster entry if this is a monster, or nil if it's actually a folder.
* **folder** *nil|MonsterFolderLua* (Read-only) Get the folder entry if this is a folder, or nil if it's actually a monster.
* **children** *MonsterNodeLua[]* 
* **parentNode** *string* 

### Functions

function **MonsterNodeLua:Duplicate**()
Create a duplicate of this entry in the bestiary.
  return *nil*

function **MonsterNodeLua:Upload**()
Save any changes made to this entry to the cloud.
  return *nil*

function **MonsterNodeLua:Delete**()
Delete this bestiary entry.
  return *nil*

function **MonsterNodeLua:ObliterateGameChanges**()
Destroy any changes made to this bestiary entry in this game. If it was first created in this game it will be destroyed and unrecoverable.
  return *nil*

function **MonsterNodeLua:MatchesSearch**(text)
Given a search string, returns true if the entry matches it.
  parametertext string
  returnboolean
