---
title: LuaShape
short_desc: LuaShape type documentation
tags: api
path: lua_api/LuaShape
uuid: 5e703f4d-47ef-785d-8df5-1f101f014659
public: true
private: false
---



### Properties

* **xpos** *number* 
* **ypos** *number* 
* **shape** *SpellShapes* 
* **radius** *number* 
* **origin** *number* 
* **locations** *Loc[]* 

### Functions

function **LuaShape:Mark**(args)
Mark this shape on the map, returning a reference that you should call Destroy() on when you want to stop displaying it.
  parameterargs {color: Color, video: nil|string, showLocs: nil|boolean}
  returnLuaObjectReference

function **LuaShape:Equal**(other)
  parameterother LuaShape
  returnboolean
