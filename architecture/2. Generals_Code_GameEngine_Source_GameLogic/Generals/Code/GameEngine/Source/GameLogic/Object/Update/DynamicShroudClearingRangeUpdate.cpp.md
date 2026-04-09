# Generals/Code/GameEngine/Source/GameLogic/Object/Update/DynamicShroudClearingRangeUpdate.cpp

## Purpose
This file implements the `DynamicShroudClearingRangeUpdate` class, which manages the dynamic shroud clearing range of game objects in Command & Conquer Generals. It handles transitions between different states (shrinking, sustaining, growing) and updates the object's vision range accordingly.

## Responsibilities
- Manages the dynamic shroud clearing range of game objects.
- Handles state transitions for shrinking, sustaining, and growing vision ranges.
- Updates grid decals to visually represent changes in vision range.
- Ensures proper cleanup and resource management.

## Key Types
- `DynamicShroudClearingRangeUpdateModuleData (struct)`: Stores configuration data for dynamic shroud clearing updates.
- `DynamicShroudClearingRangeUpdate (class)`: Manages the dynamic shroud clearing logic for game objects.

## Key Functions
### DynamicShroudClearingRangeUpdate
- Purpose: Constructor for the `DynamicShroudClearingRangeUpdate` class.
- Calls:
  - `DynamicShroudClearingRangeUpdateModuleData::buildFieldParse`
  - `getObject()->getControllingPlayer()`
  - `createGridDecals`

### update
- Purpose: Updates the shroud clearing range based on current state and time.
- Calls:
  - `animateGridDecals`
  - `killGridDecals`
  - `setShroudClearingRange`

### createGridDecals
- Purpose: Creates grid decals to visually represent changes in vision range.
- Calls:
  - `RadiusDecalTemplate::createRadiusDecal`

### animateGridDecals
- Purpose: Animates the grid decals based on current vision range and position.
- Calls:
  - `getObject()->getPosition()`
  - `m_gridDecal[d].setPosition`
  - `m_gridDecal[d].setOpacity`

### killGridDecals
- Purpose: Clears and removes all grid decals.
- Calls:
  - `m_gridDecal[d].clear`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/DynamicShroudClearingRangeUpdate.h"

- External symbols used but not defined here:
  - `TheGameLogic`
  - `GRID_FX_DECAL_COUNT`
  - `PI`
  - `INI::parseDurationUnsignedInt`
  - `INI::parseReal`
  - `RadiusDecalTemplate::parseRadiusDecalTemplate`
