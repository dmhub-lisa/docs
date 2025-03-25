---
title: DiceStudioLua
short_desc: DiceStudioLua type documentation
tags: api
path: lua_api/DiceStudioLua
uuid: afbe7110-dce2-6a5b-ba3c-6b8c0180aae2
public: true
private: false
---



### Properties

* **canSave** *boolean* 
* **uploaded** *boolean* 
* **dicePanelStyles** *any* 
* **font** *string* 
* **fontOptions** *any* 
* **border** *string* 
* **borderOptions** *any* 
* **customDiceModel** *string* 
* **customDiceModelOptions** *any* 
* **particles** *any* 
* **particleOptions** *any* 
* **curves** *any* 
* **allCurveInputs** *any* 
* **builtinMaterialProperties** *any* 
* **materialProperties** *any* 
* **textMaterialProperties** *any* 
* **showText** *any* 
* **surfaceMaterialName** *any* 
* **material** *any* 
* **finishVideoEffect** *any* 
* **availableMaterials** *any* 

### Functions

function **DiceStudioLua:Activate**()
  return *nil*

function **DiceStudioLua:Deactivate**()
  return *nil*

function **DiceStudioLua:UpdateMaterial**()
  return *nil*

function **DiceStudioLua:Save**()
  return *nil*

function **DiceStudioLua:SaveAs**(name)
  parameter **name** *string*
  return *nil*

function **DiceStudioLua:Load**(name)
  parameter **name** *string*
  return *nil*

function **DiceStudioLua:Upload**()
  return *nil*

function **DiceStudioLua:GetLocalFiles**()
  return *any*

function **DiceStudioLua:GetMaterialProperties**(id)
  parameter **id** *string*
  return *any*

function **DiceStudioLua:AddCurve**()
  return *any*

function **DiceStudioLua:GetMaterial**(id)
  parameter **id** *string*
  return *any*

function **DiceStudioLua:SpawnPreview**(nfaces)
  parameter **nfaces** *number*
  return *nil*

function **DiceStudioLua:RecordPreviewVideo**(callback)
  parameter **callback** *any*
  return *nil*
