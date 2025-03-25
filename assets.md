---
title: assets
short_desc: assets type documentation
tags: api
path: lua_api/assets
uuid: ff29f78b-74e0-ee5a-a22c-02928173467e
public: true
private: false
---



### Properties

* **coreAssetsDownloaded** *any* 
* **artists** *any* 
* **monstersRoot** *any* 
* **monsters** *any* 
* **monsterFolders** *any* 
* **allObjects** *any* 
* **themes** *any* 
* **brushes** *any* 
* **shopItems** *any* 
* **biomes** *any* 
* **tilesheets** *any* 
* **floors** *any* 
* **walls** *any* 
* **weatherEffects** *any* 
* **imagesTable** *any* 
* **imagesByTypeTable** *any* 
* **imageLibrariesTable** *any* 
* **emojiTable** *any* 
* **imageAtlasTable** *any* 
* **audioTable** *any* 
* **pdfDocumentsTable** *any* 
* **clipboardTable** *any* 
* **clipboardFoldersTable** *any* 
* **audioFoldersTable** *any* 
* **audioFoldersTableIncludingDeleted** *any* 
* **documentFoldersTable** *any* 
* **objectComponentOptions** *any* 
* **allAssets** *any* 

### Functions

function **assets:GetMonsterNode**(id)
  parameterid string
  returnMonsterNodeLua

function **assets:AddAndUploadArtist**(id)
  parameter **id** *any*
  return *nil*

function **assets:UploadNewMonsterFolder**(tableArgs)
  parameter **tableArgs** *any*
  return *nil*

function **assets:UploadNewClipboardFolder**(tableArgs)
  parameter **tableArgs** *any*
  return *nil*

function **assets:UploadNewAudioFolder**(tableArgs)
  parameter **tableArgs** *any*
  return *nil*

function **assets:GetObjectNode**(id)
  parameter **id** *string*
  return *any*

function **assets:GetObjectsWithKeyword**(keyword)
  parameter **keyword** *string*
  return *any*

function **assets:UploadNewObjectFolder**(tableArgs)
  parameter **tableArgs** *any*
  return *nil*

function **assets:UploadNewObject**(args)
  parameter **args** *any*
  return *any*

function **assets:CreateBrush**()
  return *any*

function **assets.CreateLocalShopItem**()
  return *any*

function **assets:CreateNewImageLibrary**(options)
  parameter **options** *any*
  return *string*

function **assets:FindEmojiByIdOrName**(name, emojiType)
  parameter **name** *string*
  parameter **emojiType** *string*
  return *any*

function **assets:UploadEmojiAsset**(options)
  parameter **options** *any*
  return *any*

function **assets:UploadImageAtlasAsset**(options)
  parameter **options** *any*
  return *any*

function **assets.UploadPDFDocumentAsset**(options)
  parameter **options** *any*
  return *any*

function **assets:UploadNewDocumentFolder**(tableArgs)
  parameter **tableArgs** *any*
  return *nil*

function **assets:UploadAudioAsset**(options)
  parameter **options** *any*
  return *any*

function **assets:UploadClipboardAsset**(options)
  parameter **options** *any*
  return *any*

function **assets:UploadImageAsset**(options)
  parameter **options** *any*
  return *any*

function **assets.PathSizeInBytes**(path)
  parameter **path** *string*
  return *number*

function **assets:CreateWallAssetFromFile**(options)
  parameter **options** *any*
  return *any*

function **assets:CreateTilesheetFromFile**(options)
  parameter **options** *any*
  return *any*

function **assets:CreateWeatherEffectFromFile**(options)
  parameter **options** *any*
  return *any*

function **assets:DuplicateTilesheet**(tileid)
  parameter **tileid** *any*
  return *any*

function **assets:DuplicateWall**(wallid)
  parameter **wallid** *any*
  return *any*

function **assets:ImportUniversalVTT**(pathsList, callback, error)
  parameter **pathsList** *any*
  parameter **callback** *any*
  parameter **error** *any*
  return *nil*

function **assets:CreateBestiaryEntry**()
  return *any*

function **assets:CreateBestiaryFolder**(name)
  parameter **name** *any*
  return *any*

function **assets:CreateAudioFolder**(name)
  parameter **name** *any*
  return *any*

function **assets:RefreshAssets**(cat)
  parameter **cat** *any*
  return *nil*

function **assets:LoadImageOrVideoFileLocally**(path)
  parameter **path** *any*
  return *any*
