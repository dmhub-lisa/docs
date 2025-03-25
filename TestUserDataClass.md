---
title: TestUserDataClass
short_desc: TestUserDataClass type documentation
tags: api
path: lua_api/TestUserDataClass
uuid: e39f3b01-ad2d-8854-bb17-7cb4c4a5a255
public: true
private: false
---



### Properties

* **propertyTest** *number* 

### Functions

function **TestUserDataClass:MyFunction**(x)
  parameter **x** *number?*
  return *any*

function **TestUserDataClass.Create**(x)
  parameter **x** *number*
  return *any*

function **TestUserDataClass:AddStrings**(a, b)
  parameter **a** *any*
  parameter **b** *string*
  return *string*

function **TestUserDataClass:VarArgsFunction**(a, b)
  parameter **a** *number*
  varargs: **b** *any*
  return *number*

function **TestUserDataClass:VarArgsParamsFunction**(a, b)
  parameter **a** *number*
  varargs: **b** *any*
  return *number*

function **TestUserDataClass.StaticFunction**(a, b, c)
  parameter **a** *any*
  parameter **b** *number?*
  parameter **c** *number?*
  return *number*
