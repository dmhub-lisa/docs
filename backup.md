---
title: backup
short_desc: backup type documentation
tags: api
path: lua_api/backup
uuid: 860dd054-5877-f85e-96bc-4685f58e327b
public: true
private: false
---



### Properties

* **autoBackupInterval** *number* 
* **manifest** *any* 
* **mapManifest** *any* 

### Functions

function **backup.Update**()
  return *nil*

function **backup.GetEntryInfo**(fname)
  parameter **fname** *string*
  return *any*

function **backup.BackupGame**()
  return *nil*

function **backup.BackupMap**()
  return *nil*

function **backup.DeleteBackup**(fname)
  parameter **fname** *string*
  return *nil*

function **backup.Restore**(args)
  parameter **args** *any*
  return *boolean*
