---
title: ChatMessageInfoLua
short_desc: ChatMessageInfoLua type documentation
tags: api
path: lua_api/ChatMessageInfoLua
uuid: 40e91b9c-3b5b-3550-a1f1-79f8b2e372e6
public: true
private: false
---



### Properties

* **messageType** *any* 
* **infoAndAmendments** *any* 
* **properties** *any* 
* **isComplete** *boolean* 
* **userid** *any* 
* **nick** *any* 
* **message** *any* 
* **tokenid** *any* 
* **isRoll** *any* 
* **timestamp** *any* 
* **incomplete** *any* 
* **nickColor** *any* 
* **formattedText** *any* 
* **numVisibleCharacters** *any* 
* **realtimeInteractions** *any* 
* **gmonly** *boolean* 

### Functions

function **ChatMessageInfoLua:UploadRealtimeInteraction**(userid, info)
  parameter **userid** *string*
  parameter **info** *any*
  return *nil*

function **ChatMessageInfoLua:UploadProperties**(properties)
  parameter **properties** *any*
  return *nil*

function **ChatMessageInfoLua:Delete**()
  return *nil*
