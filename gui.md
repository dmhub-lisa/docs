---
title: gui
short_desc: gui type documentation
tags: api
path: lua_api/gui
uuid: 87077004-106c-2751-99e0-299df5dcea30
public: true
private: false
---




### Functions

function **gui.Style**(args)
Create a Style
  parameterargs StyleArgs
  returnStyle

function **gui.Panel**(args)
Create a Panel
  parameterargs PanelArgs
  returnPanel

function **gui.Carousel**(table)
Create a Carousel panel
  parameterargs CarouselArgs
  returnCarousel

function **gui.MapImport**(table)
  parameter **table** *any*
  return *any*

function **gui.Table**(table)
Create a Table panel
  parameterargs TablePanelArgs
  returnTablePanel

function **gui.TableRow**(table)
Create a Row panel
  parameterargs RowPanelArgs
  returnRowPanel

function **gui.Label**(table)
Create a Label panel
  parameterargs LabelArgs
  returnLabel

function **gui.Input**(table)
Create a Input panel
  parameterargs InputArgs
  returnInput

function **gui.RegisterTheme**(themeid, sectionid, styles)
  parameter **themeid** *any*
  parameter **sectionid** *any*
  parameter **styles** *any*
  return *nil*

function **gui.CreateTheme**(themeType)
  parameter **themeType** *any*
  return *any*

function **gui.Gradient**(value)
  parameter **value** *any*
  return *any*
