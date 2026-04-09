# Generals/Code/GameEngine/Source/GameLogic/Object/Update/RadarUpdate.cpp

## Purpose
Handles the radar update logic for game objects, including extending radar range and managing its active state.

## Responsibilities
- Manages radar extension timing.
- Updates radar conditions on game objects.
- Handles serialization (CRC and Xfer) for radar data.

## Key Types
- RadarUpdateModuleData (struct): Stores radar extension time.
- RadarUpdate (class): Manages radar update logic for objects.

## Key Functions
### extendRadar
- Purpose: Initiates the radar extension process.
- Calls: 
  - `setModelConditionState`
  - `getFrame`

### update
- Purpose: Updates the radar state based on frame timing.
- Calls:
  - `clearAndSetModelConditionState`
  - `getFrame`

## Globals
None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/ModelState.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/RadarUpdate.h"
