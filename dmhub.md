---
title: dmhub
short_desc: dmhub type documentation
tags: api
path: lua_api/dmhub
uuid: d15e201a-545f-de5f-912e-996bd665b048
public: true
private: false
---



The main interface to dmhub.
### Properties

* **version** *string* The current version of the DMHub engine.
* **whiteLabel** *WhiteLabel* The current 'white label' version of the engine this is. May be 'dmhub' or 'mcdm'
* **whiteLabelEntityName** *string* The name of the publisher of the product the engine is running as.
* **whiteLabelAppName** *string* The name of the app the engine is running as, suitable for showing to users.
* **nodiagonals** *boolean* If true, the game rules are set up to have no pythagorean theorem when calculating diagonals.
* **betaBranch** *nil|string* Which branch the app is opted-in to updating from. This is not relevant if the app is being updated from Steam, Itch, or similar.
* **GetSelectedCharacters** *fun(): string[]|nil* A function that can be set to tell the engine which characters are currently selected. Returns a list of token ids.
* **GetSelectedMonster** *fun(): string|nil* A function that can be set to tell the engine which bestiary entry monster is selected. Returns a string representing the id of the bestiary entry.
* **GetSelectedObject** *fun(): string|nil* A function that can be set to tell the engine which object asset id is selected in the UI.
* **GetSelectedTerrain** *fun(): string|nil* A function that can be set to tell the engine which terrain asset id is selected in the UI.
* **GetSelectedFloor** *fun(): string|nil* A function that can be set to tell the engine which floor asset id is selected in the UI.
* **GetSelectedWall** *fun(): string|nil* A function that can be set to tell the engine which wall asset id is selected in the UI.
* **GetSelectedEffect** *fun(): string|nil* A function that can be set to tell the engine which effect asset id is selected in the UI.
* **SelectTerrain** *fun(terrainid: string): nil* 
* **SelectFloor** *fun(floorid: string): nil* 
* **SelectWall** *fun(wallid: string): nil* 
* **SelectEffect** *fun(effectid: string): nil* 
* **ObjectsSelected** *fun(objectids: string[]): nil* 
* **GetLightingInfo** *fun(floorid: string): {cacheable: boolean, indoors: Color, outdoors: Color, illumination: number, shadow: {dir: Vector2, color: Color} }* A function that can be set to tell the engine what the current lighting looks like. It will be called every frame to set the lighting.
* **ObjectEditingEnabled** *fun(): boolean* 
* **SelectionToolEnabled** *fun(): boolean* 
* **GetActiveClipboardItem** *fun(): ClipboardItem* 
* **TokenVisionUpdated** *fun(): nil* 
* **GetFocus** *fun(): Panel|nil* 
* **CreateLootComponent** *fun(): table* 
* **CreateTextComponent** *fun(): table* 
* **GetObjectInteractives** *fun(): table* 
* **ShowObjectInteractive** *any* 
* **CreateObjectInteractive** *fun(): table* 
* **CreateGameHud** *fun(container: SheetContainer, sheethud: SheetHud): Panel* 
* **DataStreamed** *fun(eventName: string, path: string, payload: string): nil* 
* **DataTransmitted** *fun(method: string, path: string, payload: string): nil* 
* **DistanceDisplayFunction** *fun(distance: number): string* Given a distance in the world, converts to a string ready to be displayed to the player.
* **RankPrimaryToken** *fun(creature: Creature): number|nil* Given a creature, this function should return a score to reflect how likely this creature is to be a player character. It is used so if a player has control of multiple tokens, to determine which one, by default, is considered their primary character.
* **GetActiveWhiteboardTool** *fun(): { tool: string, color: Color, width: Number }* 
* **CancelEditing** *fun(sheet: Sheet): boolean* 
* **GetSymbolTypesDocumentation** *fun(typename: string): nil|{name: string, type: string, desc: string}[]* 
* **IsDialogOpen** *fun(): boolean* Function that can be used to communicate to the engine whether a modal dialog is currently open.
* **SetTokenSize** *fun(token: CharacterToken, sizeid: string): nil* 
* **ShowGameContextMenu** *fun(entries: {text: string, tooltip: string, icon: string, click: fun(): nil}[]): nil* 
* **CreateKeyFrameComponent** *fun(): table* 
* **CreateEventHandlerComponent** *fun(): table* 
* **CreateEventTriggerComponent** *fun(): table* 
* **CreateDataInputComponent** *fun(): table* 
* **CreateDataOutputComponent** *fun(): table* 
* **TokensAreFriendly** *fun(a: CharacterToken, b: CharacterToken): boolean* 
* **DescribeToken** *fun(token: CharacterToken): string* 
* **DataError** *fun(message: string): nil* Function which is called by the engine when a networking error occurs allowing display of a message to the user.
* **GetHeightEditingInfo** *fun(): {opacity: number, blend: number, height: number, directional: boolean}* Editor callback function: Used to determine what height editing options the user has selected in the UI.
* **SelectHeight** *fun(height: number): nil* Editor callback function: Used when the user uses the eyedropper tool to select a height to notify the interface what height they selected.
* **GetWallHeight** *fun(): number* Editor callback function: Used to determine the height the user is currently editing walls at.
* **tokensLoggedInAs** *nil|string[]* If the GM is forcibly logged in as a token or set of tokens so they can view through their eyes, this returns a list of the token ids that the GM is logged in as.
* **tokenVision** *nil|string[]* If the GM is viewing token vision this is equal to a list of the tokenids whose vision the GM is seeing through.
* **tokenInfo** *SheetHud* 
* **diagnosticStatus** *string* (read-only) The most important diagnostic message to display to the user currently, or an empty string if there is none.
* **status** *string* (read-only) A general status message that describes the mouse's position in world space and information about the tile the user is pointing at, such as its terrain type and position.
* **uploadQuotaTotal** *number* The amount of data this user can upload each month, in bytes.
* **uploadQuotaRemaining** *number* The remaining data this user can upload this month, in bytes.
* **singleFileUploadQuota** *number* The maximum size file the user can upload, in bytes.
* **singleFilePatreonUpgradeMessage** *any* 
* **currentTerrainFill** *string|nil* The terrain background the map currently has set. Nil means no background.
* **MapExport** *MapExportCameraLua* The MapExport interface which allows export of a map to an image or video.
* **tablesUpdateId** *number* A number which increases by 1 every time the compendium assets are updated. Can save this value and then compare to it later to see if the compendium has changed at all since we last checked.
* **ngameupdate** *integer* (read-only) A sequential integer that is unique to the game being updated from the cloud. Anytime this value changes we have new data from the cloud and the game is in a different state.
* **gameupdateid** *string* (read-only) A guid that is unique to the game being updated from the cloud. Anytime this value changes we have new data from the cloud and the game is in a different state.
* **currentRollGuid** *nil|string* (Read-only) The guid that has been assigned to the current roll that is being previewed.
* **debugLog** *(string|{message: string, trace: string})[]* All debug log messages that have been recorded.
* **frozen** *boolean* If the game state is frozen. Setting this value will upload the update to the cloud immediately.
* **game** *game* (read-only) the game interface.
* **loginUserid** *string* The userid the user logged in with.
* **userid** *string* (read-only) the userid of the current user. Note that this may be the userid the game owner is impersonating within their game. @see loginUserid to get their true id.
* **userDisplayName** *string* The display name of the current user. When written to, the new display name will be sent to the cloud. Remote users will take up to a minute to reflect the new name.
* **unitsPerSquare** *number* (read-only) the measurement units per square. Typically this is 5.
* **floorid** *string* (read-only) the id of the current floor.
* **isGameOwner** *boolean* (read-only) true if the current user has ownership privileges in the game.
* **isDM** *boolean* (read-only) true if the current user has GM status in the game.
* **inGame** *boolean* (read-only) true if we are currently in-game
* **gameid** *string* (Read-only) The gameid of the current game.
* **editorMode** *boolean* (Read-only) returns true if the user is doing some kind of map/game editing, rather than in normal play mode.
* **undoState** *any* 
* **connectionErrorStatus** *any* 
* **patronTier** *number* 
* **subscriptionTier** *number* 
* **isAdminAccount** *boolean* 
* **hasStoreAccess** *boolean* (Read-only) controls whether there is a store in this version of the app.
* **networkLogLevel** *number* The log level we use for networking messages. 0 = all, 1 = information, 2 = warning, 3 = error, 4 = exception, 5 = none
* **activeObjectsPath** *string* 
* **users** *string[]* (Read-only) A list of userids of all users in the game. You may call @see GetSessionInfo to find more information about each of them.
* **allTokens** *CharacterToken[]* (Read-only) A list of all tokens active and deployed on the map.
* **selectedTokens** *CharacterToken[]* 
* **currentToken** *nil|CharacterToken* (Read-only) the token the player is assumed to be currently controlling -- the token they have control of and is selected, or their primary character. May return nil, though it won't if the player has a PC assigned to them.
* **selectedOrPrimaryTokens** *CharacterToken[]* (Read-only) a list consisting of the tokens selected, or the 'primary' token of the player if there is one. This can be used to get the token the player is presumably acting as if they perform an action. May return an empty list but does not return nil.
* **tokenHovered** *nil|CharacterToken* (Read-only) Gets the currently hovered token, or nil if there is none.
* **modKeys** *@return {ctrl: nil|boolean, alt: nil|boolean, shift: nil|boolean}* Returns which mod keys are currently depressed.
* **mouseWheel** *@return number* Returns a positive or negative number if the mousewheel has been moved this frame, based on the direction. Returns 0 if the mousewheel has not been moved this frame.
* **screenDimensions** *Vector2* 
* **uiVerticalScale** *number* 
* **uiscale** *number* (Read-only) the amount the ui is being scaled by horizontally.
* **serverTime** *number* (Read-only) The server time in seconds. Server time is designed to be the same (or at least as close as possible) across all computers connected to the game.
* **serverTimeMilliseconds** *number* (Read-only) The server time in milliseconds. Server time is designed to be the same (or at least as close as possible) across all computers connected to the game.
* **infoBubbles** *table<string, InfoBubbleHudLua>* (Read-only) The info bubbles available on the current map.
* **initiativeQueue** *nil|InitiativeQueue* The initiative queue. Note: check to make sure it's not nil and that the hidden member isn't set to check if initiative is active.
* **inCharacterSheet** *boolean* If the player is viewing their character sheet.
* **useParallax** *boolean* (Read-only) if true the app is using parallax features.
* **parallaxRatio** *number* The current parallax ratio the game is using.
* **settingsChangesRequireRestart** *boolean* If true, some important settings have been changed so the user should be urgently prompted to restart the app.
* **inCoroutine** *boolean* Returns true if we are currently running in a coroutine.
* **PlaceholderNil** *any* A stand-in for nil when we want to put it in a table.
* **debugPropertyOutput** *string* Engine debugging and performance information.

### Functions

function **dmhub.PurgePrefs**()
Purges the player's app preferences. This will wipe all settings that are stored as 'preference' type settings.
  return *nil*

function **dmhub.SanitizeDatabaseKey**(key)
This accepts a key and returns a possibly modified version of the key that makes it suitable to store in the database. All keys of tables must be safe if we are to store them in the cloud. '.', '$', '[', ']', '#', '/' and non standard ascii characters or non-printable characters are not allowed as keys that will be stored in the cloud.
  parameter **key** *string*
  return *string*

function **dmhub.UnloadMod**(instanceGuid)
Unloads the mod with the given instance guid from the game.
  parameter **instanceGuid** *string*
  return *nil*

function **dmhub.GetTypeDocumentation**(typeid)
  parametertypeid: string The name of the type to query information about.
  return{name: string, type: string, documentation: string|nil, typeSignature: string|nil}[]

function **dmhub.RegisterEventHandler**(eventName, fn)
Registers an event handler for the named global event that the engine can fire. Returns a unique id that can later be passed to @see DeregisterEventHandler to deregister and stop listening for this event.
  parametereventName string
  parameterfn fun():nil
  returnstring

function **dmhub.DeregisterEventHandler**(guid)
Deregisters an event handler, so that it is no longer managed by the event system.
  parameter **guid** *string*
  return *nil*

function **dmhub.RefreshCharacterSheet**()
Forces the character sheet to be re-built. This can be an expensive operation and is mostly designed to be used during development if you change the code driving the character sheet. Doing this unnecessarily will cause lots of character sheet slowdowns.
  return *nil*

function **dmhub.GetAudioSpectrum**()
Returns an array of numbers representing the current audio volume at each frequency. Can be used to visualize the sounds currently being emitted by the engine.
  returnnumber[]

function **dmhub.RebuildGameHud**()
This rebuilds the main user interface from scratch. It will be performance intensive and should usually only be done if we are loading and unloading mods during development.
  return *nil*

function **dmhub.GetModLoading**()
If we are currently loading a mod, returns that mod's interface. Otherwise will return nil.
  returnCodeModInterface

function **dmhub.InvalidateTokenUI**()
This rebuilds the token ui interfaces that show over tokens. Normally only used during development.
  return *nil*

function **dmhub.GetWorldSpacePanel**(floorid, panelid)
Gets a UI container suitable for putting a UI into for the given floor. panelid is a unique id you can provide for your interface name.
  parameterfloorid string
  parameterpanelid string
  returnSheetContainer

function **dmhub.CreateObjectImporter**(options)
Creates an object importer that will handle uploading objects to the cloud. paths should specify paths to image f iles containing objects. If breakup is specified, the files will automatically be broken into sheets, otherwise an image will be treated as one object. Threshold controls the sensitivity of the breakup.
  parameteroptions {path: string[], threshold: number|nil, breakup: boolean|nil}
  return ObjectImportLua

function **dmhub.OpenFileDialog**(options)
Opens an operating system file dialog. id should uniquely identify this 'kind' of file open operation. The folder the user navigates to will be saved and future calls to this function with the same id will begin in that folder. The open callback will be called once for each file opened. If multiFiles is true, then openFiles will be called with a list of files opened. If the user cancels the interaction without opening a file, the cancel callback will be called. Extensions should contain possible file types that may be open, it should be in a format like {'wav', 'mp3', 'ogg'}
  parameteroptions {id: string, extensions: string[], multiFiles: boolean, prompt: string, open: nil|(fun(path: string): nil), openFiles: nil|(fun(paths: string[]): nil), cancel: nil|(fun(): nil)}

function **dmhub.OpenFolderDialog**(value)
Opens an operating system file dialog allowing the user to open a folder. id should uniquely identify this 'kind' of file open operation. The folder the user navigates to will be saved and future calls to this function with the same id will begin in that folder. The open callback will be called and will include the folder's path and then all files within that folder that have matching extensions. Extensions should contain possible file types that may be open, it should be in a format like {'wav', 'mp3', 'ogg'}
  parameteroptions {id: string, extensions: string[], prompt: string, open: nil|(fun(folderPath: string, filePaths: string[]): nil), cancel: nil|(fun(): nil)}

function **dmhub.ParseJsonFile**(path, errorCallback)
Parses a json file at the given path, returning its parsed contents. Will return nil if an error occurred.
  parameterpath string The path to the file.
  parametererrorCallback nil|(fun(string): nil) A callback that will be called if there is an error parsing the file.
  returnany

function **dmhub.ReadTextFile**(path, errorCallback)
Reads a text file at the given path, returning its contents as a string. Will return nil if an error occurred.
  parameterpath string The path to the file.
  parametererrorCallback nil|(fun(string): nil) A callback that will be called if there is an error parsing the file.
  returnstring|nil

function **dmhub.ParseDocxFile**(path, errorCallback)
Parses a Word/docx file at the given path, returning its parsed contents as a string in an html-like form. Will return nil if an error occurred.
  parameterpath string The path to the file.
  parametererrorCallback nil|(fun(string): nil) A callback that will be called if there is an error parsing the file.
  returnstring|nil

function **dmhub.FillTerrain**(terrainid)
Sets the terrain background of the current map. Passing in nil will clear the background.
  parameterterrainid: string|nil

function **dmhub.SetMapTool**(toolInfo)
Sets the map tool that is currently being used when the user is moused over the map.
  parametertoolInfo MapToolInfo
  returnEventSourceLua
--- --- @class MapToolInfo--- @field tool 'free'|'objectpoints'|'forbidden' The name of the tool to use.--- @field expires number The amount of time the tool will be set to, suggested to set to 0.5 or less.--- @field closed boolean If true then the tool will be along a closed path.
function **dmhub.SaveImageDialog**(options)
Open a system file dialog inviting the user to save a file as an image. The named texture will be saved.
  @field options {texture: string, error: (fun(message: string): nil)}

function **dmhub.RemoveAndUploadImageFromLibrary**(libraryName, imageid)
Remove an image from an image library. Changes will be synced to cloud.
  parameter **libraryName** *string*
  parameter **imageid** *string*
  return *nil*

function **dmhub.AddAndUploadImageToLibrary**(libraryName, imageid)
Upload an image to the cloud.
  parameter **libraryName** *string*
  parameter **imageid** *string*
  return *nil*

function **dmhub.SearchImages**(searchString, libraryName)
  parametersearchString string The string to search for.
  parameterlibraryName string|nil The library to search for.
  returnstring[] A list of image id's which match the search.

function **dmhub.SearchSounds**(searchString)
  parametersearchString string The string to search for.
  returnstring[] A list of audio id's which match the search.

function **dmhub.ObliterateTableItem**(tableName, id)
This deletes an item from a table. If the item was created in this game, it will be completely removed and can't be undeleted. If it is from a module it will be hidden in this game.
  parameter **tableName** *string*
  parameter **id** *string*
  return *nil*

function **dmhub.SetAndUploadTableItem**(tableName, item, options)
  parametertableName string The name of the table the item is in.
  parameteritem table The item to upload to the table.
  parameteroptions nil|{ deferUpload: boolean, success: (fun():nil), failure: (fun(message: string): nil) }
  returnstring

function **dmhub.GetTableTypes**()
Get all of the data tables that have been registered. These are all the possible values that  can be passed as the tableName parameter to @see SetAndUploadTableItem and @see GetTable
  returnstring[]

function **dmhub.GetTable**(tableName)
Get the specified data table. Returns nil if the table does not exist or is empty. Note that the return table includes items that are 'hidden' -- have been deleted by the user.
  parametertableName string
  returntable<string, table>

function **dmhub.GetTableVisible**(tableName)
Get the specified data table. Returns nil if the table does not exist or is empty. Excludes table items that are 'hidden'.
  parametertableName string
  returntable<string, table>

function **dmhub.SearchTable**(tableName, searchString, options)
  parametertableName string The name of the table
  parametersearchString the string to search for.
  parameteroptions {fields: string[]} Fields can specify a list of fields that will be searched, rather than searching all fields.
  returntable<string, table>

function **dmhub.RunWithModuleAssets**(moduleScope, fn)
The given function is run. While the function is running, the module provided will be the only whose assets are available to inspect.
  parametermoduleScope string The module id of the module.
  parameterfn (fun(): nil) A function to execute.

function **dmhub.CreateCanvasOnMap**(options)
Creates a panel on the map at the given point.
  parameteroptions {point: Vector3, sheet: Panel}
  returnSheetContainer

function **dmhub.MarkRadius**(table)
Mark an area on the map. You can provide a set of locations to the center argument, and can also specify a radius if you want to expand out from those locations. Call Destroy() on the returned object when you want to destroy the marker.
  parameterradius number|nil Default=1
  parametercolor Color
  parametercenter Loc[]
  returnLuaObjectReference

function **dmhub.MarkLocs**(args)
Mark a set of locations on the map. Call Destroy() on the returned object when you want to destroy the marker.
  parametercolor Color
  parameterlocs Loc[]
  returnLuaMultiObjectReference

function **dmhub.CalculateShape**(args)
Create an object describing a shape on the map.
  parameterargs {shape: SpellShapes, token: CharacterToken, targetPoint: Vector3, range: nil|number, radius: nil|number, locOverride: nil|Loc, requireEmpty: nil|boolean }
  returnLuaShape

function **dmhub.RegisterRollBonusType**(name)
Registers a bonus type used with rolls, e.g. "Circumstance" for circumstance bonuses in pf2e. Once registered, dice rolls may use these identifiers as keywords to identify the type of a bonus.
  parameter **name** *string*
  return *nil*

function **dmhub.ClearRollBonusTypes**()
Clears all roll bonus types that have been registered. This would typically be done in a module where you want to clear out the game system and start fresh.
  return *nil*

function **dmhub.Roll**(rolldef)
Execute a dice roll. Returns an object that manages the roll.
  parameterrolldef RollDefinition
  returnnil|ActiveRollLua

function **dmhub.CancelCurrentRoll**()
Cancels out the current dice roll we are previewing. (Doesn't cancel rolls that have already begun)
  return *nil*

function **dmhub.ParseRoll**(text, lookupFunction, options)
  parametertext string
  parameterlookupFunction function
  parameternil|table options
  return{exploding = nil|boolean, categories = table<string, {mod=number, groups={numDice=number, numFaces=number, numKeep=number,subtract=nil|boolean}[]}>}

function **dmhub.RollToString**(rollInfo)
  parameter **rollInfo** *any*
  return *string*

function **dmhub.NormalizeRoll**(text, lookupFunction, reason, options)
Normalize a roll into a standard, human-readable format.
  parametertext string The roll text.
  parameterlookupFunction nil|function
  parameterreason nil|string
  parameteroptions nil|table
  @result string

function **dmhub.GetRollAdvantage**(text)
  parameter **text** *string*
  return *string*

function **dmhub.ForceRollAdvantage**(text, advantageState)
  parameter **text** *string*
  parameter **advantageState** *string*
  return *string*

function **dmhub.RollExpectedValue**(text)
  parameter **text** *string*
  return *number*

function **dmhub.RollMinValue**(text)
  parameter **text** *string*
  return *number*

function **dmhub.RollMaxValue**(text)
  parameter **text** *string*
  return *number*

function **dmhub.RegisterGoblinScriptDebugger**(callbackFunction)
  parameter **callbackFunction** *any*
  return *nil*

function **dmhub.EvalGoblinScript**(goblinscript, lookupFunction, reason)
Evaluates the given goblinscript as much as possible, looking up any strings and returns the script reduced to hopefully just a dice roll or even numeric result. Always returns a string with a best effort to reduce the formula.
  parametergoblinscript string
  parameterlookupFunction function
  parameterreason string
  @result string

function **dmhub.EvalGoblinScriptToObject**(goblinscript, lookupFunction, reason)
This evaluates the given goblinscript string with the support of the lookup function which can be used to lookup the value of symbols. The goblinscript should not contain any dice rolls. It will evaluate to a Lua object containing the result. It might be, for instance, a creature or an ability.
  parametergoblinscript string
  parameterlookupFunction function
  parameterreason nil|string

function **dmhub.EvalGoblinScriptDeterministic**(goblinscript, lookupFunction, defaultValue, reason)
This evaluates the given goblinscript string with the support of the lookup function which can be used to lookup the value of symbols. The goblinscript should not contain any dice rolls. It will be forced to a numeric result even if there are errors or illicit dice rolls.
  parametergoblinscript string
  parameterlookupFunction function
  parameterdefaultValue nil|number
  parameterreason nil|string

function **dmhub.ExplainDeterministicGoblinScript**(goblinscript, lookupFunction, explainFunction)
  param goblinscript string
  parameterlookupFunction function
  parameterexplainFunction fun(symbol: string, has: boolean): string
  returnnil|(string[])

function **dmhub.AutoCompleteGoblinScript**(args)
Given some goblin script generates possible completions for the code.
  parameterargs {text: string, symbols: nil|table, deterministic: nil|boolean}
  returnnil|({word: string, completion: string, type: string, desc: string}[])

function **dmhub.IsRollDeterministic**(text, lookupFunction)
Returns true if the given formula is deterministic, not involving any actual dice rolls.
  parametertext string
  parameterlookupFunction function
  returnboolean

function **dmhub.RollInstant**(text, lookupFunction)
Makes an instant roll and returns the result. The lookupFunction will be used to evaluate any GoblinScript included in the text.
  parametertext string
  parameterlookupFunction function
  returnnumber

function **dmhub.RollInstantCategorized**(text)
Make a roll with an instant result. It won't be logged or visualized. The result is returned. It will be broken into categories (though most rolls will just have one category)
  parametertext string the dice roll to make. e.g. '1d6+4'
  @result table<string,number>

function **dmhub.DragDice**(roll)
Call this while the user is dragging the mouse. Indicates they are dragging dice and will spawn the given dice under their mouse with them dragging them.
  parameter **roll** *string*
  return *nil*

function **dmhub.Debug**(msg)
Log a debug message. A trace will be included with it. This is the main way to perform debug output (using the print() function calls this)
  parameter **msg** *string*
  return *nil*

function **dmhub.CloudError**(msg)
Log an error to the cloud for developers to review.
  parameter **msg** *string*
  return *nil*

function **dmhub.Error**(msg)
Log an error message.
  parameter **msg** *string*
  return *nil*

function **dmhub.DuplicateWindowInNewProcess**()
Execute another instance of the app connected to the same game.
  return *nil*

function **dmhub.SyncCamera**(options)
Forces other user's cameras to move to this user's camera position.
  parameteroptions {speed: nil|number} The speed the camera should move (default=1)

function **dmhub.ToJson**(val)
Convert a lua value to json.
  parameter **val** *any*
  return *string*

function **dmhub.DeepCopy**(val)
Makes a deep copy of val and returns it.
  parameter **val** *any*
  return *any*

function **dmhub.DeepEqual**(a, b)
Performs a deep comparison on a and b and returns true if they are completely equal.
  parametera any
  parameterb any
  returnboolean

function **dmhub.GetDiff**(a, b)
Creates a patch that is required to transfer 'a' to 'b' and returns it. Returns nil if the two values are identical.
  parametera any
  parameterb any
  returnany

function **dmhub.Patch**(subject, patch)
Patches the first object with the second, returning true if any changes occurred, and false otherwise.
  parametersubject any
  parameterpatch any
  returnboolean

function **dmhub.Time**()
The number of seconds since the app started. @see serverTime for a time that will be consistent with other users.
  return *number*

function **dmhub.FrameCount**()
The number of frames the app has been running for.
  return *number*

function **dmhub.Log**(msg)
Log the given message locally to the chat panel.
  parameter **msg** *string*
  return *nil*

function **dmhub.Execute**(cmd)
Executes the given command.
  parameter **cmd** *string*
  return *nil*

function **dmhub.Eval**(cmd)
Evaluates the given lua code.
  parameter **cmd** *string*
  return *nil*

function **dmhub.GetBuiltinBindings**()
Gets the default bindings used by the app.
  returntable<string, {command: string, name: string, section: string, dmonly: boolean}>

function **dmhub.GetCommandBinding**(cmd, context)
Get the keystroke that is bound to the given command. If the context is given it will only be within that context.
  parametercmd string
  parametercontext nil|string
  returnnil|string

function **dmhub.SetCommandBinding**(keystroke, cmd, context)
Sets the given keystroke to be bound to the given command. If context is given it will only be set in the named context.
  parameter **keystroke** *string*
  parameter **cmd** *string*
  parameter **context** *string?*
  return *nil*

function **dmhub.DetectBindableKeystroke**()
If a bindable keystroke is currently depressed, returns it.
  returnnil|string

function **dmhub.ResetKeybindings**()
Reset all keybindings to defaults.
  return *nil*

function **dmhub.GetFriendsList**()
Gets a table full of users that the current user might be considered 'friends' with -- as in have shared a game with those users.
  returntable<string,{games: string[], aliases: string[]}>

function **dmhub.UpdateScreenHudArea**(delay)
After the given delay, recalculates the area of the screen that the map should be drawn in.
  parameter **delay** *number*
  return *nil*

function **dmhub.PushUserRichStatus**(statusText, previousid)
Sets the 'rich status' displayed for this user. Returns a value which can be passed to @see PopUserRichStatus to remove this rich status. Any number of rich status can be set, and the most recent one that hasn't been removed will display.
  parameterstatusText string
  parameterpreviousid nil|string If given, will pop the rich status with this id before pushing the new status.
  returnstring

function **dmhub.PopUserRichStatus**(luaid)
This removes the rich status message with the id previously returned from @PushUserRichStatus.
  parameterluaid nil|number

function **dmhub.GetDisplayName**(userid)
Gets the display name the user has chosen for themself.
  parameteruserid string
  returnstring

function **dmhub.IsUserOwner**(userid)
Check if the given user is the owner of the game.
  parameteruserid string
  returnboolean

function **dmhub.IsUserDM**(userid)
Check if the given user is a GM.
  parameteruserid string
  returnboolean

function **dmhub.SetDMStatus**(userid, status)
Sets whether the given user is a GM. Must have correct permissions for this to succeed.
  parameter **userid** *string*
  parameter **status** *boolean*
  return *nil*

function **dmhub.KickPlayer**(userid)
Kicks the player with the given userid from the game. Must have permissions for this to be successful.
  parameter **userid** *string*
  return *nil*

function **dmhub.GetPartyInfo**(partyid)
  parameterpartyid string
  returnLuaPartyInfo

function **dmhub.GetPlayerInfo**(userid, beginChanges)
Gets game information about the player with the given userid. If beginChanges is true, notifies that we intend to modify the returned value and then will use @see UploadPlayerInfo to upload changes to the cloud.
  parameteruserid string
  parameterbeginChanges nil|boolean (default=false)
  returnLuaGamePlayerDetails

function **dmhub.UploadPlayerInfo**(userid)
After calling @see GetPlayerInfo() and modifying the player info this will upload the modified data to the cloud.
  parameter **userid** *string*
  return *nil*

function **dmhub.RegisterRemoteEvent**(eventid, callback)
Listens for the named eventid to be triggered, with the given callback being called when it is. @see BroadcastRemoteEvent for more details.
  parametereventid string A unique eventid identifying the event.
  parametercallback function

function **dmhub.BroadcastRemoteEvent**(eventid, sessionid, args)
This broadcasts an event to connected computers using the peer-to-peer mechanism. Because it uses peer-to-peer there is no guarantee the messages will arrive. They should be used to communicate transient information that will go out of date quickly, such as the user's mouse position, what they are highlighting, etc. If multiple messages using the same sessionid arrive out of order, the old messages will be discarded and not processed. 
  parametereventid string A unique eventid identifying the event.
  parametersessionid A unique id identifying a 'session' which can receive multiple messages. If you want to broadcast multiple events concerning the same topic, use the same sessionid.
  parameterargs any

function **dmhub.RegisterEscapePriority**(key, value)
Registers a named priority for escape listening. The named key is associated with the given priority level.
  parameter **key** *string*
  parameter **value** *number*
  return *nil*

function **dmhub.GetInputForCommand**(cmd)
Given a command, returns a list of any hotkey presses that will trigger that command.
  parametercmd string
  returnstring[]

function **dmhub.ImportObjects**()
  return *nil*

function **dmhub.ImportBattleMap**()
  return *nil*

function **dmhub.AddObjectFolder**()
  return *string*

function **dmhub.LeaveGame**()
Leaves the current game back to the titlescreen
  return *nil*

function **dmhub.ShowPlayerSettings**()
  return *nil*

function **dmhub.Undo**()
Undo the last user editing action.
  return *nil*

function **dmhub.Redo**()
Redo the last user editing action.
  return *nil*

function **dmhub.ElevateToDM**(isDM)
Elevates the user to GM status or removes their GM status. Only works on admin accounts.
  parameter **isDM** *any*
  return *nil*

function **dmhub.OpenTutorialVideo**(id)
Open the tutorial video with the given id.
  parameter **id** *string*
  return *nil*

function **dmhub.OpenArtistPage**(artist)
Open the page for the given content creator's web page.
  parameter **artist** *string*
  return *nil*

function **dmhub.OpenImageAssetURL**(imageid)
Open the image asset with the given id in a web browser.
  parameter **imageid** *string*
  return *nil*

function **dmhub.OpenRegisteredURL**(urlName)
Opens a known registered URL from the list of known url's.
  parameter **urlName** *string*
  return *nil*

function **dmhub.OpenURL**(url)
Open the given URL in a web browser. Only links to certain approved domains will be allowed for security reasons.
  parameter **url** *string*
  return *nil*

function **dmhub.OverrideMouseCursor**(cursorid, duration)
Forces the mouse cursor to the given mouse cursor. Lasts for 'duration' time. You may call this again and again to refresh periodically.
  parametercursorid MouseCursor
  parameterduration number

function **dmhub.RefreshMapLayout**()
Force recalculation of map layout. This does not normally need to be called, though may be used for debugging purposes if the map doesn't update after making a change.
  return *nil*

function **dmhub.GetSessionInfo**(userid)
  parameteruserid The userid of the user to get session info concerning.
  returnLuaGameSession

function **dmhub.PingUser**(userid, callback, callbackPeerToPeer)
  parameteruserid string The userid of the user to ping.
  parametercallback (fun(): any) The callback to call when the pong is received. This means a message will have been sent to the cloud, the cloud notified the other user, and the user responded via the cloud.
  parametercallbackPeerToPeer (fun(): any) The call when the peer-to-peer pong is received. This means a direct message was sent from this computer to the other computer. Sometimes peer-to-peer connections don't work and this may not be called.

function **dmhub.GetTokensAtLoc**(loc)
Returns all tokens that are at the given location. For tokens larger than one location, it will return them if any part of them is in the location.
  parameterloc Loc
  returnnil|CharacterToken[]

function **dmhub.GetTokens**(options)
If options is nil, this will return a list of all tokens on the map. Otherwise, will return all the tokens that meet the criteria given in the options. playerControlled = all tokens controlled by players. playerControlledNotShared = all tokens controlled by players, but doesn't include 'party controlled' tokens. haveProperties means tokens that have non-nil CharacterToken.properties. This is largely deprecated since all CharacterTokens should now have properties. unaffiliated means monsters, tokens not controlled by the players or any party. pending refers to tokens that are currently being added but may not have been transferred to the cloud yet (this state should be very brief, less than a second). If position is given, then only tokens within radius of the position will be returned. This function may return an empty list if there are no tokens that match the criteria, but it will not return nil.
  parameteroptions nil|{playerControlled: nil|boolean, playerControlledNotShared: nil|boolean, haveProperties: nil|boolean, unaffiliated: nil|boolean, pending: nil|boolean, position: {x: number, y: radius: radius: number}}
  returnCharacterToken[]

function **dmhub.LookupToken**(properties)
Given a token's Lua properties (the CharacterToken.properties member, which is most often a Creature) returns the CharacterToken if found.
  parameterproperties table
  returnnil|CharacterToken

function **dmhub.LookupTokenId**(properties)
Given a token's Lua properties (the CharacterToken.properties member, which is most often a Creature) returns the tokenid of the token if found.
  parameterproperties table
  returnnil|string

function **dmhub.GetTokenById**(id)
Gets the token associated with the given tokenid. This only searches live tokens that are currently spawned on the map, so it will have to be on the map that is currently loaded. Otherwise nil will be returned. @see GetCharacterById to get a token anywhere in the game.
  parametertokenid string
  returnnil|CharacterToken

function **dmhub.GetCharacterIdsInParty**(partyid)
Returns a list of all the tokenid's in the given party. Returns an empty list if the party is empty or if the party doesn't exist.
  parameterpartyid string The id of the party to get token ids for.
  returnstring[]

function **dmhub.GetCharacterById**(tokenid)
Gets the token associated with the given tokenid. This retrieves the token as long as it is defined anywhere in the game, it need not be spawned in the map.
  parametertokenid string
  returnnil|CharacterToken

function **dmhub.CreatureSizeToTokenScale**(creatureSize)
  parametercreatureSize string
  returnnumber

function **dmhub.Assert**(cond)
  parametercond boolean

function **dmhub.RegisterSetting**(info)
Registers a new setting.
  parameterinfo {id: string, storage: SettingStorage, default: any, enum: nil|any[], format: nil|string, invalidatesStyles: nil|boolean}

function **dmhub.HasSetting**(settingid)
Returns true if the given setting id exists.
  parameter **settingid** *string*
  return *boolean*

function **dmhub.GetSettingValue**(settingid)
Get the value of a game setting.
  parameter **settingid** *string*
  return *any*

function **dmhub.ResetSetting**(settingid)
Reset the given setting to its default value.
  parameter **settingid** *string*
  return *boolean*

function **dmhub.SetSettingValue**(settingid, val, lockValue)
Sets the game setting to the given value. 
  parametersettingid string
  parameterval any
  @paral lockValue nil|boolean

function **dmhub.PreviewSettingValue**(settingid, val)
Sets a game setting, but only locally, not transferring it yet. This is a good idea to do if e.g. the user is dragging a slider but hasn't committed to the change yet.
  parameter **settingid** *string*
  parameter **val** *any*
  return *nil*

function **dmhub.KeyPressed**(keycode)
Returns true if the given key is currently depressed.
  parameterkeycode KeyCode
  returnboolean

function **dmhub.SetDraggingObject**()
Notifies the engine that an object is being dragged from the object palette. This will be cleared when the engine detects that the user releases the mouse.
  return *nil*

function **dmhub.SetDraggingMonster**()
Notifies the engine that a monster is being dragged from the bestiary. This will be cleared when the engine detects that the user releases the mouse.
  return *nil*

function **dmhub.GenerateGuid**()
Generate a new guid -- a unique, random string.
  returnstring

function **dmhub.FormatTimestamp**(timestamp, formatstr)
Format a timestamp as an attractive display and returns it.
  parametertimestamp number
  parameterformatstr string|nil Defaults to 'yyyy-MM-dd HH:mm:ss'
  returnstring

function **dmhub.ViewSign**(imageid)
Shows the given image as a modal that fills most of the screen.
  parameterimageid string

function **dmhub.Schedule**(delay, fn)
After delay seconds elapses, fn will be executed.
  parameterdelay number
  parameterfn (fun(): any)

function **dmhub.ScheduleWhen**(predicate, fn)
Arranges for predicate to be called every frame. The first time it returns true, fn is executed.
  param predicate (fun(): boolean)
  parameterfn (fn(): any)

function **dmhub.CenterOnToken**(tokenid, callback)
Center on the token with the given id, calling the callback when complete.
  parametertokenid string
  parametercallback (fun(): nil)
  returnboolean

function **dmhub.SelectToken**(charid)
Select the token with the given id, clearing selection of other tokens.
  parameter **charid** *string*
  return *nil*

function **dmhub.AddTokenToSelection**(tokenid)
Add the token with the given id to the selection.
  parameter **tokenid** *string*
  return *nil*

function **dmhub.PulseHighlightToken**(tokenid)
Momentarily highlights the token with the given id.
  parameter **tokenid** *string*
  return *nil*

function **dmhub:UploadInitiativeQueue**()
Tranmit changes to the initiative queue to the cloud.
  return *nil*

function **dmhub.HaveImageInClipboard**()
Query if there is a valid image in the system clipboard.
  return *boolean*

function **dmhub.CopyToClipboard**(text)
Copies the given text to the system clipboard.
  parameter **text** *string*
  return *nil*

function **dmhub.CopyToInternalClipboard**(obj)
Sets the contents of the internal clipboard.
  parameter **obj** *any*
  return *nil*

function **dmhub.GetInternalClipboard**()
The contents of the internal clipboard used when copying and pasting.
  any

function **dmhub.CloseCharacterSheet**()
  return *any*

function **dmhub.GetPlayerActionRequests**()
  return *any*

function **dmhub.GetPlayerActionRequest**(id)
  parameter **id** *any*
  return *any*

function **dmhub.SendActionRequest**(info)
  parameter **info** *any*
  return *any*

function **dmhub.CancelActionRequest**(id)
  parameter **id** *any*
  return *nil*

function **dmhub.QuitApplication**()
Quit the application.
  return *nil*

function **dmhub.SendRecoverPasswordEmail**(email)
Try to recover the user's password to the supplied email address.
  parameter **email** *string*
  return *nil*

function **dmhub.Login**(username, password, remember)
Logs the user in with the supplied credentials.
  parameter **username** *string*
  parameter **password** *string*
  parameter **remember** *boolean*
  return *nil*

function **dmhub.Logout**()
Logs the user out.
  return *nil*

function **dmhub.TryAutoLogin**()
Attempt to automatically login using saved credentials. Returns true if we have saved credentials to login with.
  return *boolean*

function **dmhub.Coroutine**(fn, args)
Starts running 'fn' as a coroutine with the given arguments.
  parameterfn (fun(): nil)
  @vararg args any

function **dmhub.CoroutineSynchronous**(fn, args)
Starts running 'fn' as a coroutine with the given arguments. If already in a coroutine it will run synchronously. If we are inside a dmhub call (e.g. CharacterToken.ModifyProperties) it will wait until the end of the execution of that call before running the coroutine code immediately after.
  parameterfn (fun(): nil)
  @vararg args any

function **dmhub.Stopwatch**()
Creates a stopwatch object which can be used to measure time.
  returnLuaStopwatch

function **dmhub.ProfileMarker**(name)
Create a marker for profiling purposes.
  returnLuaProfileMarker

function **dmhub.CreateNetworkOperation**()
Call this to signal an important network operation is occurring which should lock the app behind an unskippable dialog until it's complete. Set progress on the returned object to set the percentage complete. When set to 1 the operation will complete and UI disappear.
  returnNetworkOperationStatus

function **dmhub.ClearSelectedObjects**()
Clear all objects from being selected.
  return *nil*

function **dmhub.GetCoverInfo**(attacker, target)
Given an attacker and a target, gets information about how much cover exists between them.
  parameterattacker CharacterToken
  parametertarget CharacterToken
  return{cover: number, coverModifier: number, description: string}

function **dmhub.GetAttackTrajectory**(attacker, target, sourcePos, outcomeType)
Given an attack with a given outcome, will calculate a good path for a missile to go from the source to the target to make an appealing animation for the user.
  parameterattacker CharacterToken
  parametertarget CharacterToken
  parametersourcePos Vector2
  parameteroutcomeType AttackOutcome
  return{sourcePoint: Vector2, destPoint: Vector2, obstructionPoint: Vector2}

function **dmhub.GetMouseWorldPoint**()
Get the position of the mouse in world coordinates.
  returnVector2

function **dmhub.HighlightLine**(options)
Highlights the line between a and b. Call Destroy() on the returned reference to remove the highlighted line.
  parameteroptions {color: nil|Color, a: Vector2, b: Vector2, floorIndex: number?}
  returnLuaTargetingMarkers

function **dmhub.MarkLineOfSight**(attacker, target)
Mark the line of sight between the attacker and target on the map. Call Destroy() on the returned reference to clear the marker.
  parameterattacker CharacterToken
  parametertarget CharacterToken
  returnLuaTargetingMarkers

function **dmhub.ease**(t, easing)
  parametert number A value between 0 and 1.
  parametereasing Easing The easing to use.
  returnnumber

function **dmhub.HasStylus**()
Returns true if a stylus of some kind is available as an input device.
  return *boolean*

function **dmhub.GetDiceStyling**(diceset, colorStr)
Query what colors a dice set uses so we can draw a UI representation of it.
  parameterdiceset nil|string The dice set to query the dice styling for. Default='default'
  parametercolorStr nil|string An optional color to style the dice with, if this dice set allows dice coloring.
  return{trimcolor: string, bgcolor: string, color: string}

function **dmhub.BeginTransaction**()
When called, all network changes will be delayed until @see EndTransaction is called and then all changes will be made at once.
  return *nil*

function **dmhub.EndTransaction**()
Should be paired with a call to @see BeginTransaction. Will commit all changes since BeginTransaction was called.
  return *nil*

function **dmhub.tr**(text, options)
Translates the given string using the translation system, returning the translated string. If there is no translation available or we the language is set to English, the string will be returned unaltered.
  parametertext string
  returnstring
