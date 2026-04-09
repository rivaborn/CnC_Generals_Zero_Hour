# Generals/Code/GameEngine/Source/GameClient/Drawable/Update/SwayClientUpdate.cpp

## Purpose
Handles client-side tree sway animation based on wind/breeze parameters.

## Responsibilities
- Updates sway parameters based on breeze info
- Applies rotation to drawable objects for sway effect
- Manages sway state (enabled/disabled)
- Serializes sway data for network sync
- Handles post-load initialization

## Key Types
- `SwayClientUpdate` (Class): Manages tree sway animation logic
- `BreezeInfo` (Struct): Contains wind/breeze parameters (external)

## Key Functions
### `updateSway`
- Purpose: Updates sway parameters from current breeze info
- Calls: `TheScriptEngine->getBreezeInfo()`, `GameClientRandomValueReal`

### `clientUpdate`
- Purpose: Applies sway rotation to the drawable object
- Calls: `getDrawable()`, `TheScriptEngine->getBreezeInfo()`, `updateSway()`, `Cos`, `getObject()`, `getStatusBits()`

### `xfer`
- Purpose: Serializes sway module state for network transfer
- Calls: `ClientUpdateModule::xfer`, `xfer->xferReal`, `xfer->xferShort`, `xfer->xferBool`

### `loadPostProcess`
- Purpose: Initializes sway parameters after loading
- Calls: `ClientUpdateModule::loadPostProcess`, `updateSway`

## Globals
- None

## Dependencies
- `Drawable.h`, `Module/SwayClientUpdate.h`, `Player.h`, `ThingFactory.h`, `RandomValue.h`, `Xfer.h`, `Object.h`, `ScriptEngine.h`, `GameLogic.h`
- `TheScriptEngine` (external), `GameClientRandomValueReal` (external), `PI` (external), `Cos` (external)
