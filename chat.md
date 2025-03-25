---
title: chat
short_desc: chat type documentation
tags: api
path: lua_api/chat
uuid: 7d6fe031-fe89-9a59-8e6c-0affe198748c
public: true
private: false
---



### Properties

* **events** *EventSourceLua* An event source that you can subscribe to for chat events.
* **messages** *ChatMessageInfoLua[]* All messages in the chat.

### Functions

function **chat.DiceEvents**(guid)
Given a dice roll, returns an event source you can subscribe to to get events for the dice.
  parameterguid string
  returnEventSourceLua

function **chat.Send**(message)
Send a message to the chat.
  parametermessage string

function **chat.SendCustom**(panel)
Send a CustomChatPanel to chat.
  parameterpanel CustomChatPanel
  returnstring The guid of the message.

function **chat.UpdateCustom**(key, properties)
Updates a CustomChatPanel in chat. The key is the guid previously returned by @see SendCustom
  parameterkey string
  parameterproperties CustomChatPanel

function **chat.ShareData**(data)
Share a game object (e.g. a spell, ability, or item) to the chat.
  parameterdata table

function **chat.ShareObjectInfo**(tableid, objid, properties)
  parameter **tableid** *string*
  parameter **objid** *string*
  parameter **properties** *any?*
  return *nil*

function **chat.Clear**()
Clear the chat.
  return *nil*

function **chat.PreviewChat**(message)
  parameter **message** *any*
  return *nil*

function **chat.GetCommandCompletions**(command)
  parameter **command** *string*
  return *any*

function **chat.GetRollInfo**(key)
  parameter **key** *string*
  return *any*
