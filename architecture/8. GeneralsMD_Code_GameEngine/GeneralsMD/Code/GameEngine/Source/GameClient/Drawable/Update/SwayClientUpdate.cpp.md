# GeneralsMD/Code/GameEngine/Source/GameClient/Drawable/Update/SwayClientUpdate.cpp

## Purpose
Handles client-side tree sway animation based on wind/breeze parameters.

## Responsibilities
- Updates sway parameters from script engine breeze info
- Applies rotation transformations to drawable objects
- Manages sway state (enabled/disabled)
- Serializes/deserializes sway data for network sync
- Handles burned object sway termination

## Key Types
- **SwayClientUpdate (Class)**: Manages tree sway animation logic
- **BreezeInfo (Struct)**: Contains wind parameters (intensity, direction, etc.)

## Key Functions
### `updateSway()`
- Purpose: Updates sway parameters from current breeze info
- Calls: `TheScriptEngine->getBreezeInfo()`, `GameClientRandomValueReal()`

### `clientUpdate()`
- Purpose: Applies sway rotation to drawable object each frame
- Calls: `updateSway()`, `getDrawable()`, `isVisible()`, `getInstanceMatrix()`, `setInstanceMatrix()`, `getObject()`, `getStatusBits()`

### `xfer()`
- Purpose: Serializes/deserializes sway module state
- Calls: `ClientUpdateModule::xfer()`, `xferVersion()`, `xferReal()`, `xferShort()`, `xferBool()`

## Globals
- None

## Dependencies
- `Drawable.h`, `Module/SwayClientUpdate.h`, `Player.h`, `ThingFactory.h`, `RandomValue.h`, `Xfer.h`, `Object.h`, `ScriptEngine.h`, `GameLogic.h`
