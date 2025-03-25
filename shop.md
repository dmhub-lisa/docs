---
title: shop
short_desc: shop type documentation
tags: api
path: lua_api/shop
uuid: d301908d-6a2c-3d50-9592-1a77115050f3
public: true
private: false
---



### Properties

* **events** *any* 
* **inventoryItems** *any* 

### Functions

function **shop:ItemInInventory**(itemid)
  parameter **itemid** *string*
  return *boolean*

function **shop:AcknowledgeNewInventoryItems**()
  return *any*

function **shop:CheckoutSubscription**(tier)
  parameter **tier** *number*
  return *nil*

function **shop:Checkout**(items, args)
  parameter **items** *any*
  parameter **args** *any*
  return *nil*

function **shop:QueryGiftCode**(code, callback, errorCallback)
  parameter **code** *string*
  parameter **callback** *any*
  parameter **errorCallback** *any*
  return *nil*

function **shop:AdminSetGiftCodeNote**(code, note)
  parameter **code** *string*
  parameter **note** *string*
  return *nil*

function **shop:AdminCreateGiftCode**(code, data)
  parameter **code** *string*
  parameter **data** *any*
  return *nil*

function **shop:MonitorItemGiftCodes**(itemid)
  parameter **itemid** *string*
  return *any*

function **shop:RetrieveGiftCodes**(callback, errorCallback, completeCallback)
  parameter **callback** *any*
  parameter **errorCallback** *any*
  parameter **completeCallback** *any*
  return *number*
