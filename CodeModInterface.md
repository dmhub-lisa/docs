---
title: CodeModInterface
short_desc: CodeModInterface type documentation
tags: api
path: lua_api/CodeModInterface
uuid: 0e791946-9012-015b-a400-55a8a07722ba
public: true
private: false
---



### Properties

* **isowner** *boolean* 
* **canedit** *boolean* 
* **modid** *string* 

### Functions

function **CodeModInterface:GetDocumentPath**(id)
  parameter **id** *string*
  return *any*

function **CodeModInterface:GetDocumentSnapshot**(id)
  parameter **id** *string*
  return *any*

function **CodeModInterface:OpenDocumentDebugURL**(docid)
  parameter **docid** *string*
  return *nil*

function **CodeModInterface:SaveDefaultDocuments**(callback)
  parameter **callback** *any*
  return *nil*

function **CodeModInterface:CallEnterGame**()
  return *nil*

function **CodeModInterface:GlobalStyle**(t)
  parameter **t** *any*
  return *nil*

function **CodeModInterface:RecordEventHandlerInstance**(eventName, guid)
  parameter **eventName** *string*
  parameter **guid** *string*
  return *nil*
