---
title: ImageAsset
short_desc: ImageAsset type documentation
tags: api
path: lua_api/ImageAsset
uuid: a7a1f104-68d1-c758-92ee-24c5e2e6042f
public: true
private: false
---

 : [:GameAsset](/lua_api/ImageAsset)

### Properties

* **previewSpriteRect** *any* 
* **isVideo** *boolean* 
* **isLoadedAndVideo** *any* 
* **sprite** *any* 
* **sizeInKBytes** *number* 
* **textureCached** *boolean* 
* **textureReadable** *boolean* 

### Functions

function **ImageAsset:ValidationCheck**(objtype, guid)
  parameter **objtype** *string*
  parameter **guid** *string*
  return *boolean*

function **ImageAsset:MatchesSearch**(searchLowercase)
  parameter **searchLowercase** *string*
  return *boolean*

function **ImageAsset:OnBeforeLoadImage**()
  return *nil*

function **ImageAsset:GetPivot**(tex)
  parameter **tex** *any*
  return *any*

function **ImageAsset:GetPPU**(tex)
  parameter **tex** *any*
  return *number*

function **ImageAsset:SyncSprite**(priority, pin)
  parameter **priority** *any?*
  parameter **pin** *boolean?*
  return *nil*

function **ImageAsset:GetAndPollTexture**(pin)
  parameter **pin** *boolean?*
  return *any*

function **ImageAsset:GetAndPollTexture**(cacheable, error, videoPlayer, pin)
  parameter **cacheable** *any*
  parameter **error** *any*
  parameter **videoPlayer** *any*
  parameter **pin** *boolean?*
  return *any*

function **ImageAsset:GetAndPollTexture**(videoPlayer)
  parameter **videoPlayer** *any*
  return *any*

function **ImageAsset:GetAndPollUniqueTexture**(id, videoPlayer)
  parameter **id** *string*
  parameter **videoPlayer** *any*
  return *any*

function **ImageAsset:MakeLiveEditSession**()
  return *any*

function **ImageAsset:TryEvictTexture**()
  return *boolean*

function **ImageAsset:ForceTextureReadable**()
  return *nil*
