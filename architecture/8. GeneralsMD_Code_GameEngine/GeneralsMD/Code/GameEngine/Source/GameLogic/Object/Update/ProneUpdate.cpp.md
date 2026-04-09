# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/ProneUpdate.cpp

## Purpose
Handles the "prone" state behavior for game objects, including damage-based prone duration and visual/effects management.

## Responsibilities
- Manages prone state duration based on damage taken
- Controls prone-related visual effects and object status flags
- Handles serialization (Xfer) and CRC for network sync
- Provides INI field parsing for module data

## Key Types
- **ProneUpdateModuleData (Class)**: Stores prone-related module configuration (e.g., damage-to-frames ratio)
- **ProneUpdate (Class)**: Implements prone behavior logic for game objects
- **None**: No enums/structs defined

## Key Functions
### `ProneUpdate::update`
- Purpose: Decrements prone frame counter and stops effects when prone ends
- Calls: `stopProneEffects`

### `ProneUpdate::goProne`
- Purpose: Applies prone state based on damage info
- Calls: `startProneEffects`, `getProneUpdateModuleData`

### `ProneUpdate::startProneEffects`
- Purpose: Activates prone visuals and disables attacking
- Calls: `getObject`, `getDrawable`, `setModelConditionState`, `setStatus`

### `ProneUpdate::stopProneEffects`
- Purpose: Removes prone visuals and re-enables attacking
- Calls: `getObject`, `getDrawable`, `clearModelConditionState`, `clearStatus`

### `ProneUpdate::xfer`
- Purpose: Serializes prone state for network sync
- Calls: `UpdateModule::xfer`, `xfer->xferVersion`, `xfer->xferInt`

## Globals
- **None**

## Dependencies
- `PreRTS.h`, `Common/Xfer.h
