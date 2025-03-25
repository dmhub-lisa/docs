---
title: audio
short_desc: audio type documentation
tags: api
path: lua_api/audio
uuid: 9c91d86e-04e2-a550-a3ad-8630a4fab694
public: true
private: false
---



### Properties

* **events** *any* 
* **muted** *any* 
* **masterVolume** *any* 
* **currentlyPlaying** *any* 
* **numPlayingSounds** *any* 
* **numActiveSoundEvents** *any* 

### Functions

function **audio.UploadMuted**()
  return *nil*

function **audio.UploadMasterVolume**()
  return *nil*

function **audio.StopAllSoundEvents**()
  return *nil*

function **audio.StopSoundEvent**(guid)
  parameter **guid** *string*
  return *nil*

function **audio.PreviewSoundEventVolume**(guid, volume)
  parameter **guid** *any*
  parameter **volume** *any*
  return *nil*

function **audio.SetSoundEventVolume**(guid, volume)
  parameter **guid** *any*
  parameter **volume** *any*
  return *nil*

function **audio.PlaySoundEvent**(options)
  parameter **options** *any*
  return *any*
