---
title: LuaCore
short_desc: LuaCore type documentation
tags: api
path: lua_api/LuaCore
uuid: 53492353-22c4-2b53-af12-514f4d4cb191
public: true
private: false
---




### Functions

function **LuaCore.Color**(value)
Examples:
core.Color('#ff0000'): create a red color.
core.Color('#00ff00bb'): create a green color that is partly translucent.
core.Color{ r = 1, g = 0, b = 0 }: creates a red color.
core.Color{ h = 0.3, s = 0.8, v = 0.8 }: creates a color hue shifted 30%, saturation of 80%, and value of 80%.
core.Color{ h = 0, s = 0, v = 5 }: creates a super bright white.
  parametervalue string|table
  returnColor

function **LuaCore.Loc**(value)
Creates a Loc which specifies a location on the map.
  parametervalue { x: number, y: number, floorIndex?: number, tinyLoc?: number }
  returnLoc

function **LuaCore.Vector2**(x, y)
Create a Vector2.
  parameterx number
  parametery number
  returnVector2

function **LuaCore.Vector3**(x, y, z)
Create a Vector3.
  parameterx number
  parametery number
  parameterz number
  returnVector3

function **LuaCore.Vector4**(x, y, z, w)
Create a Vector4.
  parameterx number
  parametery number
  parameterz number
  parameterw number
  returnVector4

function **LuaCore.PopulateTooltipAlignmentFromDirection**(dir, output)
Will set the halign and valign keys in the output table based on the direction specified by 'dir'.
  parameterdir Vector2 A direction.
  parameteroutput A table to populate with halign and valign keys.
