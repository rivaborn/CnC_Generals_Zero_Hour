# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/RadarUpdate.cpp

## Purpose
Handles radar extension and state updates for objects in the game.

## Responsibilities
- Manages radar extension timing and state transitions
- Updates radar visual conditions on drawable objects
- Handles serialization/deserialization of radar state
- Provides CRC and Xfer support for network sync

## Key Types
- `RadarUpdateModuleData` (Class): Stores radar extension duration
- `RadarUpdate` (Class): Manages radar update logic for objects

## Key Functions
### `extendRadar`
- Purpose: Initiates radar extension with visual and timing logic
- Calls: `getRadarUpdateModuleData`, `getObject`, `getDrawable`, `setModelConditionState`, `TheGameLogic->getFrame`

### `update`
- Purpose: Updates radar state based on frame timing
- Calls: `TheGameLogic->getFrame`, `getObject`, `getDrawable`, `clearAndSetModelConditionState`

### `xfer`
- Purpose: Serializes/deserializes radar state for network sync
- Calls: `UpdateModule::xfer`, `xfer->xferVersion`, `xfer->xferUnsignedInt`, `xfer->xferBool`

## Globals
- None

## Dependencies
- `PreRTS.h`, `ModelState.h`, `Xfer.h`, `Drawable.h`, `GameLogic.h`, `Object.h`, `RadarUpdate.h`
- `UpdateModule`, `Thing`, `Xfer`, `TheGameLogic`, `Drawable`, `MODELCONDITION_RADAR_EXTENDING`, `MODELCONDITION_RADAR_UPGRADED`
