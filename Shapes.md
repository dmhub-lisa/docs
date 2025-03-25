---
title: Shapes
short_desc: Shapes type documentation
tags: api
path: lua_api/Shapes
uuid: 8a02e875-1379-2e59-9778-95b466dd201f
public: true
private: false
---



### Properties

* **pencolor** *any* 
* **thickness** *any* 

### Functions

function **Shapes:AddLine**(node)
  parameter **node** *any*
  return *any*

function **Shapes:AddPath**(node)
  parameter **node** *any*
  return *any*

function **Shapes:AddDisc**(node)
  parameter **node** *any*
  return *any*

function **Shapes:GetCurvePoints**(controlPoints, numResults)
  parameter **controlPoints** *any*
  parameter **numResults** *any*
  return *any*

function **Shapes:SetColor**(shapeid, color)
  parameter **shapeid** *any*
  parameter **color** *any*
  return *nil*

function **Shapes:Remove**(id)
  parameter **id** *any*
  return *nil*

function **Shapes:PushStyle**()
  return *nil*

function **Shapes:PopStyle**()
  return *nil*
