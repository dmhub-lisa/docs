---
title: DiceMaterialStudioProperties
short_desc: DiceMaterialStudioProperties type documentation
tags: api
path: lua_api/DiceMaterialStudioProperties
uuid: 06eb8eac-ea3b-8d5d-b111-3fa6363d1757
public: true
private: false
---




### Functions

function **DiceMaterialStudioProperties:Clone**()
  return *any*

function **DiceMaterialStudioProperties:ToDebugString**()
  return *string*

function **DiceMaterialStudioProperties:GetFloat**(s, defaultValue)
  parameter **s** *string*
  parameter **defaultValue** *any*
  return *number*

function **DiceMaterialStudioProperties:GetColor**(s)
  parameter **s** *string*
  return *any*

function **DiceMaterialStudioProperties:GetTexture**(s, index)
  parameter **s** *string*
  parameter **index** *any*
  return *any*

function **DiceMaterialStudioProperties:HasTextureArray**(s)
  parameter **s** *string*
  return *boolean*

function **DiceMaterialStudioProperties:CreateTextureArray**(s)
  parameter **s** *string*
  return *nil*

function **DiceMaterialStudioProperties:DestroyTextureArray**(s)
  parameter **s** *string*
  return *nil*

function **DiceMaterialStudioProperties:SetFloat**(s, f)
  parameter **s** *string*
  parameter **f** *number*
  return *nil*

function **DiceMaterialStudioProperties:SetColor**(s, c)
  parameter **s** *string*
  parameter **c** *any*
  return *nil*

function **DiceMaterialStudioProperties:SetTexture**(s, t, index)
  parameter **s** *string*
  parameter **t** *string*
  parameter **index** *any*
  return *nil*

function **DiceMaterialStudioProperties.DiceFacesToIndex**(numFaces)
  parameter **numFaces** *number*
  return *number*
