---
title: PDFDocument
short_desc: PDFDocument type documentation
tags: api
path: lua_api/PDFDocument
uuid: c4670be5-ed43-3a52-bc41-e1ea350fbb0c
public: true
private: false
---



### Properties

* **summary** *PDFSummary* 

### Functions

function **PDFDocument:TextInRect**(npage, left, top, right, bottom, callback)
  parameter **npage** *number*
  parameter **left** *number*
  parameter **top** *number*
  parameter **right** *number*
  parameter **bottom** *number*
  parameter **callback** *any*
  return *nil*

function **PDFDocument:TextLayout**(npage, callback)
  parameter **npage** *number*
  parameter **callback** *any*
  return *nil*

function **PDFDocument:Search**(searchText)
  parametersearchText string
  return{page: number, index: number}[]

function **PDFDocument:RenderToData**(npage, width, height, region, callback)
  parameter **npage** *number*
  parameter **width** *any*
  parameter **height** *any*
  parameter **region** *any*
  parameter **callback** *any*
  return *nil*

function **PDFDocument:GetPageImageId**(npage)
  parameter **npage** *number*
  return *string*

function **PDFDocument:GetPageThumbnailId**(npage)
  parameter **npage** *number*
  return *string*
