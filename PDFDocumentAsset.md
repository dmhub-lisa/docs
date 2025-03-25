---
title: PDFDocumentAsset
short_desc: PDFDocumentAsset type documentation
tags: api
path: lua_api/PDFDocumentAsset
uuid: 548432af-1fbe-3359-98ed-beb929fd36fe
public: true
private: false
---

 : [:GameAsset](/lua_api/PDFDocumentAsset)

### Properties

* **hasBookmarks** *boolean* 
* **cachePath** *string* 

### Functions

function **PDFDocumentAsset:SetBookmarks**(toc, parentGuid, level)
  parameter **toc** *any*
  parameter **parentGuid** *string?*
  parameter **level** *number?*
  return *nil*

function **PDFDocumentAsset:Sync**()
  return *boolean*
