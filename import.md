---
title: import
short_desc: import type documentation
tags: api
path: lua_api/import
uuid: 48f642d9-5786-875d-8731-2e368ed92d9f
public: true
private: false
---



### Properties

* **importers** *any* 
* **importedAssets** *any* 
* **pendingUpload** *boolean* 
* **error** *any* 
* **uploadCostKB** *number* 
* **haveEnoughBandwidth** *boolean* 

### Functions

function **import.CreateImporter**()
  return *any*

function **import:BookmarkLog**()
  return *number*

function **import:IsReimport**(asset)
  parameter **asset** *any*
  return *boolean*

function **import:GetAssetLog**(asset)
  parameter **asset** *any*
  return *any*

function **import:GetImage**(asset)
  parameter **asset** *any*
  return *any*

function **import:StoreLogFromBookmark**(bookmark, asset)
  parameter **bookmark** *number*
  parameter **asset** *any*
  return *nil*

function **import:GetLog**()
  return *any*

function **import:CreateCharacter**()
  return *any*

function **import:CreateMonster**()
  return *any*

function **import:CreateMonsterFolder**(description)
  parameter **description** *string*
  return *any*

function **import:GetExistingItem**(tableName, itemName)
  parameter **tableName** *string*
  parameter **itemName** *string*
  return *any*

function **import:GetImports**()
  return *any*

function **import:Log**(text)
  parameter **text** *any*
  return *nil*

function **import:OnImportConfirmed**(fn)
  parameter **fn** *any*
  return *nil*

function **import:ImportMonsterFolder**(asset)
  parameter **asset** *any*
  return *nil*

function **import:ImportMonster**(asset)
  parameter **asset** *any*
  return *nil*

function **import:ImportCharacter**(asset)
  parameter **asset** *any*
  return *string*

function **import:ImportAsset**(tableName, asset)
  parameter **tableName** *string*
  parameter **asset** *any*
  return *nil*

function **import:SetImportRemoved**(id, remove)
  parameter **id** *string*
  parameter **remove** *boolean*
  return *nil*

function **import:CompleteImportStep**()
  return *boolean*

function **import.Register**(options)
  parameter **options** *any*
  return *nil*

function **import:GetCurrentImporter**()
  return *any*

function **import:ImportPlainText**(text)
  parameter **text** *string*
  return *nil*

function **import:ImportFromText**(text)
  parameter **text** *string*
  return *nil*

function **import:SetActiveImporter**(importerid)
  parameter **importerid** *any*
  return *nil*

function **import:ImportFromJson**(obj, filename)
  parameter **obj** *any*
  parameter **filename** *any*
  return *nil*

function **import:ImportImageFromURL**(url, success, error, options)
  parameter **url** *string*
  parameter **success** *any*
  parameter **error** *any*
  parameter **options** *any*
  return *nil*

function **import:ClearState**()
  return *nil*
