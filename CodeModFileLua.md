---
title: CodeModFileLua
short_desc: CodeModFileLua type documentation
tags: api
path: lua_api/CodeModFileLua
uuid: 6eaae830-823e-0c54-8e7f-ebda5e0187ab
public: true
private: false
---



### Properties

* **hasMerge** *boolean* 
* **valid** *boolean* 
* **hasLocalChanges** *boolean* 
* **localContents** *any* 
* **revisions** *any* 
* **numRevisions** *any* 
* **changeTimestamp** *any* 
* **name** *string* 

### Functions

function **CodeModFileLua:MatchesSearch**(search, options)
  parameter **search** *string*
  parameter **options** *any*
  return *boolean*

function **CodeModFileLua:MergeLocal**()
  return *boolean*

function **CodeModFileLua:SyncLocally**(revision)
  parameter **revision** *any*
  return *nil*

function **CodeModFileLua:LaunchExternalDiffWithLocal**()
  return *nil*
