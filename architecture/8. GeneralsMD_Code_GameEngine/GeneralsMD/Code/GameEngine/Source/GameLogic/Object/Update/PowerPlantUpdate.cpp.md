# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/PowerPlantUpdate.cpp

## Purpose
Handles the update logic for power plant objects, including rod extension/retraction animations and state management.

## Responsibilities
- Manages power plant rod extension/retraction animations
- Controls model condition states for visual upgrades
- Handles update timing and sleep states
- Serializes/deserializes power plant state via Xfer
- Manages wake/sleep cycles for performance

## Key Types
- **PowerPlantUpdateModuleData (Class)**: Stores module-specific data (e.g., rod extension time)
- **PowerPlantUpdate (Class)**: Main update module handling power plant behavior

## Key Functions
### `extendRods(Bool extend)`
- Purpose: Extends or retracts power plant rods with visual state changes
- Calls: `getPowerPlantUpdateModuleData()`, `getObject()`, `getDrawable()`, `setModelConditionState()`, `clearModelConditionFlags()`, `setWakeFrame()`

### `update()`
- Purpose: Finalizes rod extension by updating model conditions
- Calls: `getObject()`, `getDrawable()`, `clearAndSetModelConditionState()`

### `xfer(Xfer *xfer)`
- Purpose: Serializes/deserializes power plant state
- Calls: `UpdateModule::xfer()`, `xferVersion()`, `xferBool()`

## Globals
- None

## Dependencies
- `PreRTS.h`, `ModelState.h`, `Xfer.h`, `Drawable.h`, `InGameUI.h`, `GameLogic.h`, `Object.h`, `PowerPlantUpdate.h`
- `UpdateModule`, `Thing`, `Drawable`, `Xfer`, `XferVersion`
