---
title: ChatMessageDiceRollInfoLua
short_desc: ChatMessageDiceRollInfoLua type documentation
tags: api
path: lua_api/ChatMessageDiceRollInfoLua
uuid: fe621f6a-3982-b851-9f4d-aa18dc048aff
public: true
private: false
---

 : [:ChatMessageInfoLua](/lua_api/ChatMessageDiceRollInfoLua)

### Properties

* **messageType** *string* 
* **formattedText** *string* Nicely formatted text describing the roll.
* **waitingOnDice** *boolean* True if we don't have dice information yet about this roll.
* **timeRemaining** *number* The projected time remaining for the dice to finish rolling. If @see waitingOnDice returns true we don't have this value yet and it will return -1.
* **isComplete** *boolean* Indicates that the roll is finished.
* **resultInfo** *table<string,{mod: number, total: number, rolls: {guid: string, partnerguid: string, roll: number, faces: number, multiply: nil|number, subtract: boolean}}>* 
* **diceStyle** *any* 
* **advantage** *boolean* 
* **disadvantage** *boolean* 
* **rolls** *{guid: string, result: number, numFaces: number, dropped: boolean, explodes: boolean, category: string}[]* 
* **tiers** *number* 
* **boons** *number* 
* **banes** *number* 
* **total** *number* 
* **categories** *any* 
* **numVisibleCharacters** *any* 
* **token** *any* 
* **naturalRoll** *number* The result of the roll only including the 'natural' component. i.e. the actual dice rolled.
* **nat1** *boolean* 
* **forcedResult** *boolean* 
* **autosuccess** *boolean* 
* **autofailure** *boolean* 
* **nat20** *boolean* 
* **autocrit** *boolean* 
* **playerName** *string* 
* **playerColor** *string* 
* **description** *string* 
* **rollStr** *any* 
* **result** *string* 
