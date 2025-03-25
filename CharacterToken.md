---
title: CharacterToken
short_desc: CharacterToken type documentation
tags: api
path: lua_api/CharacterToken
uuid: c24bbd5b-6ed3-0f56-8adb-512183432770
public: true
private: false
---



### Properties

* **charid** *string* The charid (also known as tokenid) of the token/character. Uniquely identifies this token.
* **debugInfo** *string* A summary of this token suitable for outputting to a debug log.
* **monitorPath** *string* (Read-only) The 'path' within the game's cloud storage that this token resides at. If you want to see if this token has changed, you can monitor that path. @see Panel.monitorGame
* **hasTokenOnAnyMap** *boolean* If this token is deployed on a map somewhere.
* **summonerid** *nil|string* (Read-only) the tokenid of the token that summoned this token, if there is one.
* **mountObject** *nil|LuaObjectComponent* The object that this token is mounted on. e.g. sitting on a chair.
* **mountedOn** *nil|string* The tokenid of the token this token is mounted on.
* **saddleUnlocked** *boolean* If mounted on a saddle, returns true if that saddle is in the 'unlocked' state.
* **selfOrMount** *CharacterToken* (Read-only) If mounted on a token, returns the token mounted on. Otherwise is equal to this token itself.
* **mount** *nil|CharacterToken* The token we are mounted on, if there is one.
* **valid** *boolean* (Read-only) true if this token is still valid. If saving a reference to a CharacterToken between frames, this should be checked before using it. It will become invalid if the token is deleted.
* **ModifyProperties** *@param options {execute: (fun():nil), undoable: nil|boolean, combine: nil|boolean, description: nil|string}* This allows you to modify the @see properties of this token and upload it to the cloud. Inside the execute function you supply you should modify the properties of the token. This will observe the changes you make and upload only the diffs. If combine is true the upload will try to occur as a transaction with any other uploads happening this frame. Note that this only uploads the @see properties of the token. It doesn't upload the rest of the token details such as appearance. @see UploadToken to upload the full token.
* **uploadable** *boolean* (Read-only) If true, this is a normal CharacterToken that can be uploaded to the cloud service.
* **appearanceVariationIndex** *number* Which appearance variation the token is currently using.
* **numAppearanceVariations** *number* The number of appearance variations this token has.
* **saddlePositions** *Vector2[]* 
* **tokenScale** *number* 
* **saddles** *number* 
* **saddleSize** *string* 
* **saddleSizeNumber** *number* 
* **dataPath** *string* Synonym for @see monitorPath
* **playerNameOrNil** *nil|string* (Read-only) The name of trhe player controlling this token, or nil if there is none.
* **playerName** *string* (Read-only) The name of the player controling this token. Will result in 'NPC Ally' or 'NPC/Monster' if not controlled by a player.
* **ownerId** *nil|string* The userid of the player who owns this token, 'PARTY' if the token is owned by a party, nil if the token is GM-controlled. If 'PARTY' then @see partyId to get the partyid of the controlling party.
* **partyId** *nil|string* The id of the party that controls this token, if they are controlled by a party.
* **playerColor** *Color* (Read-only) the color of the player who owns this token. White if not controlled by a player.
* **playerControlled** *boolean* (Read-only) True if this token is controlled by a player, or by the player's party.
* **playerControlledNotShared** *boolean* (Read-only) True if this token is controlled directly by a player.
* **canControl** *boolean* (Read-only) True if the current user has permissions to control this token (either because they own it, it is in their party, or they are the GM)
* **primaryCharacter** *boolean* (Read-only) True if this is the primary character of the current user.
* **playerControlledAndPrimary** *boolean* (Read-only) True if this is the primary character of a player.
* **activeControllerId** *nil|string* (Read-only) the userid of the user who is best suited to responding to prompts on this token right now. Will return nil if the current user is the best suited to responding to prompts on this character.
* **canSee** *boolean* (Read-only) True if the current user can see this token (it's in their vision).
* **sheet** *Panel* The panel that is attached to this token to display their UI.
* **canRotate** *boolean* 
* **name** *string* 
* **namePrivate** *boolean* Whether the name of the token is hidden from players.
* **canLocalPlayerSeeName** *boolean* 
* **description** *string* 
* **squeezed** *boolean* If the token is currently squeezed in a tight spot.
* **posWithLean** *Vector2* (Read-only) Where the token should be positioned accounting for how it might be 'leaning' to get line of sight.
* **altitudeInDeciTiles** *integer* (Read-only) The altitude of the token in tenths of a tile. This is the altitude above the bottom of the bottom floor on the map.
* **altitude** *integer* (Read-only) The altitude of the token in tiles. This is the altitude above the bottom of the bottom floor on the map.
* **floorAltitude** *integer* (Read-only) The altitude of the token in tiles. This is relative to the 'zero point' altitude on the current floor.
* **characterHeight** *number* (read-only) the number of tiles tall the token is.
* **loc** *Loc* (Read-only) The location the token is at.
* **locsOccupying** *Loc[]* (Read-only) An array of locations the token is occupying. The number of items in this array will be based on the token's creature size.
* **mapid** *string* (Read-only) the id of the map the token is currently on.
* **floorid** *string* (Read-only) the id of the floor the token is currently on.
* **isFriendOfPlayer** *boolean* 
* **properties** *Creature* The token's lua properties representing game-specific character information. Often this is of type @see Creature
* **anthem** *nil|string* 
* **anthemVolume** *number* 
* **portraitFrameHueShift** *number* 
* **portraitFrameSaturation** *number* 
* **portraitFrameBrightness** *number* 
* **portraitFrame** *nil|string* 
* **portrait** *string* 
* **popoutPortrait** *boolean* 
* **popoutScale** *number* 
* **portraitBackground** *nil|string* 
* **appearance** *CharacterAppearance* (Read-only) Information about the character's appearance.
* **wieldedObjectsOverride** *nil|{mainhand: nil|string, offhand: nil|string, belt: nil|string}* 
* **invisibleToPlayers** *boolean* 
* **portraitRect** *Vector4* The rectangle within the portrait to display for this token.
* **radiusInTiles** *number* The radius of the token, in tiles.
* **pos** *Vector2* (Read-only) The world position the token is at.
* **posWithParallax** *Vector2* (Read-only) The world position the token is at, including adjustments due to parallax.
* **portraitZoom** *number* 
* **portraitOffset** *Vector2* 
* **creatureSize** *string* (Read-only) the size of the creature.
* **creatureSizeNumber** *number* (Read-only) the creature size as a 1-based number.
* **creatureDimensions** *Vector2* (Read-only) The width/height of the token.
* **chargeDistance** *any* 
* **lookAtMouse** *boolean* 
* **floorIndex** *number* 
* **initiativeStatus** *InitiativeStatus* (Read-only) the initiative status of the token.

### Functions

function **CharacterToken.IsPreviewToken**(id)
Returns true if this token id is not a 'real' in game token but instead a preview token shown to an in app camera.
  parameter **id** *string*
  return *boolean*

function **CharacterToken:BeginChanges**(reentrant)
(Deprecated): @see ModifyProperties instead.
  parameter **reentrant** *any*
  return *nil*

function **CharacterToken:CompleteChanges**(description, options)
(Deprecated): @see ModifyProperties instead.
  parameter **description** *string*
  parameter **options** *any*
  return *nil*

function **CharacterToken:UploadToken**(description)
Upload any changes to the token to the cloud. Note that if you are only modifying @see properties you should use @see ModifyProperties instead.
  parameter **description** *string*
  return *nil*

function **CharacterToken:RefreshAppearanceLocally**()
Refresh the appearance if it has changed. This should happen automatically so only use for debugging purposes if a token isn't updating the way you expect.
  return *nil*

function **CharacterToken:UploadAppearance**()
Upload the @see appearance section of the token.
  return *nil*

function **CharacterToken:SwitchAppearanceVariation**(nindex)
  parameter **nindex** *number*
  return *nil*

function **CharacterToken:DeleteAppearanceVariation**(index)
  parameter **index** *number*
  return *nil*

function **CharacterToken:GetVariationInfo**(index)
  parameterindex integer The index of the appearance variation to query.
  return{portrait: string, portraitFrame: string, portraitFrameHueShift: number, portraitFrameSaturation: number, portraitFrameBrightness: number, portraitBackground: nil|string, anthem: nil|string, anthemVolume: number}

function **CharacterToken:Flip**()
Flip the direction the token is facing horizontally.
  return *nil*

function **CharacterToken:GetNameMaxLength**(maxLen)
  parameter **maxLen** *number*
  return *string*

function **CharacterToken:DescribeRollAgainst**(rollStr)
  parameter **rollStr** *string*
  return *string*

function **CharacterToken:PosAtLoc**(loc)
Where the token should be positioned if it's standing at the given location.
  parameterloc Loc
  returnVector3

function **CharacterToken:LocsOccupyingWhenAt**(loc)
The locations this token would occupy if it was at the given location.
  parameterloc Loc
  returnLoc[]

function **CharacterToken:GetFallInfoFromLoc**(location)
Given a location this token wants to move to, returns nil if the token wouldn't fall when moving there, otherwise returns information about the fall.
  parameterlocation Loc
  returnnil|{floorIndex: number, label: string, loc: Loc}

function **CharacterToken:MoveVertical**(newAltitude)
Move the token vertically to the new altitude.
  parameter **newAltitude** *number*
  return *nil*

function **CharacterToken:Move**(loc, options)
  parameterloc Loc The location to move to.
  parameteroptions {maxCost: nil|number, straightline: nil|boolean, moveThroughFriends: nil|boolean, ignoreFalling: nil|boolean, movementType: nil|MovementType}
  returnnil|LuaPath

function **CharacterToken:Teleport**(loc, teleportMount)
Teleport the token to the target location.
  parameterloc Loc
  parameterteleportMount boolean Teleport the mount also if this creature is mounted.

function **CharacterToken:SwapPositions**(targetToken)
Make the token swap positions with the target token.
  parametertargetToken CharacterToken

function **CharacterToken:IsFriend**(other)
  parameterother CharacterToken
  returnboolean

function **CharacterToken:InvalidateObjects**()
Refresh any objects attached to the token.
  return *nil*

function **CharacterToken:GetPortraitRectForAspect**(aspect)
aspect is the width as a percentage of the height. e.g. 0.5 = width is half of height.
  parameteraspect float
  returnVector4

function **CharacterToken:GetGroundMoveType**(preferWater)
Returns walk of swim depending on the type of movement the creature will have to move on the ground. preferWater is used if the token straddles water and land and chooses the preferred type for the token.
  parameterpreferWater boolean
  return'walk'|'swim'

function **CharacterToken:ShowSheet**(tabid)
Reveals the token's character sheet, going to the given tab by default
  parameter **tabid** *string*
  return *nil*

function **CharacterToken:GetLineOfSight**(otherToken)
The vision of the other token you have. 1 = full vision. 0 = complete occlusion. 0.5 = half visible.
  parameter **otherToken** *any*
  return *number*

function **CharacterToken:Distance**(otherTokenOrLoc)
The distance in native units to a loc or another token.
  parameterotherTokenOrLoc CharacterToken|Loc
  @result number

function **CharacterToken:GetNearbyTokens**(radiusLua)
  parameterradius number Radius in native units (default=one tile)
  returnCharacterToken[]

function **CharacterToken:GetAurasTouching**()
  returnAura[]

function **CharacterToken:ForcedPush**(pushingToken, distanceInFeet)
  parameter **pushingToken** *any*
  parameter **distanceInFeet** *number*
  return *nil*

function **CharacterToken:RunFunctionAtLoc**(lualoc, fn)
  parameter **lualoc** *any*
  parameter **fn** *any*
  return *any*

function **CharacterToken:CalculatePathfindingArea**(movementAllowanceDecis)
  parametermovementAllowanceDecis
  returntable<{x: number, y: number}, {loc: Loc, cost: number}>

function **CharacterToken:AnimateAttack**(options)
  parameteroptions {targetid: string, rollid: string, damage: integer, outcome: AttackAnimOutcome}

function **CharacterToken:ConsumeClick**()
  return *nil*

function **CharacterToken:Render**(args, options)
Renders this token's creature into a tooltip panel and returns it.
  parameterargs table
  parameteroptions table
  @result nil|Panel

function **CharacterToken:MarkMovementRadius**(movementAllowance, args)
Renders a movement radius marker showing how far the token can move. Returns a reference controlling it. Remember to call Destroy on it when you want the radius to disappear!
  parametermovementAllowance movement allowance in decitiles.
  returnLuaMultiObjectReference

function **CharacterToken:MarkMovementArrow**(targetLoc, options)
Draw a movement arrow. @see ClearMovementArrow to clear the movement arrow.
  parametertargetLoc Loc
  parameteroptions nil|table
  returnnil|{path: LuaPath, collideWith: CharacterToken[]}

function **CharacterToken:ClearMovementArrow**()
  return *nil*
