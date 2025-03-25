---
title: AssetNodeBaseLua
short_desc: AssetNodeBaseLua type documentation
tags: api
path: lua_api/AssetNodeBaseLua
uuid: 75e01ff4-6aa6-525c-91d7-aa065b7ebf98
public: true
private: false
---



### Properties

* **hidden** *boolean* True if the entry has been 'hidden' in this game (i.e. deleted, but can be undeleted)
* **artist** *string* The content creator who created this content.
* **imageFileId** *string* 
* **ord** *number* 
* **description** *any* 
* **parentFolder** *string* 
* **parentNode** *any* 
* **children** *any* 

### Functions

function **AssetNodeBaseLua:Backup**()
Returns a json representation of this node.
  returnstring

function **AssetNodeBaseLua:Restore**(json)
Restores this from json.
  parameter **json** *string*
  return *nil*

function **AssetNodeBaseLua:OpenImageUrl**()
Open the image for this content in a web browser.
  return *nil*

function **AssetNodeBaseLua:MatchesSearch**(text)
  parameter **text** *any*
  return *any*

function **AssetNodeBaseLua:GetNodeIdsMatchingSearch**(text)
  parameter **text** *any*
  return *any*
