# Generals/Code/GameEngine/Source/GameLogic/Object/Contain/GarrisonContain.cpp

## Purpose
This file implements the logic for garrisoning objects within structures in Command & Conquer Generals, including managing positions, health effects, and AI interactions.

## Responsibilities
- Manage garrison points within structures.
- Handle object placement and removal from garrison points.
- Update garrison state based on damage conditions.
- Support AI pathfinding and attack range checks for garrisoned units.

## Key Types
- **GarrisonContainModuleData (Struct)**: Stores data related to garrisoning, such as allowed kinds of objects, healing properties, and initial roster.
- **MUZZLE_FLASH_LIFETIME (Enum)**: Defines the lifetime of muzzle flash effects in logic frames.

## Key Functions
### calcDistSqr
- Purpose: Calculates squared distance between two 3D coordinates.
- Calls: None

### findClosestFreeGarrisonPointIndex
- Purpose: Finds the closest free garrison point index to a target position.
- Calls: `calcDistSqr`

### getObjectGarrisonPointIndex
- Purpose: Returns the garrison point index for a given object.
- Calls: None

### putObjectAtGarrisonPoint
- Purpose: Places an object at a specified garrison point.
- Calls: `TheThingFactory->findTemplate`, `TheThingFactory->newDrawable`

### findConditionIndex
- Purpose: Determines the condition index based on the body damage state of the structure.
- Calls: None

### calcBestGarrisonPosition
- Purpose: Calculates the best garrison position for an object.
- Calls: `findClosestFreeGarrisonPointIndex`

### attemptBestFirePointPosition (Object version)
- Purpose: Attempts to move a unit to the best fire point position and checks attack range.
- Calls: `getObjectGarrisonPointIndex`, `putObjectAtBestGarrisonPoint`, `weapon->isWithinAttackRange`

### attemptBestFirePointPosition (Coord3D version)
- Purpose: Similar to above, but uses a target position instead of an object.
- Calls: `getObjectGarrisonPointIndex`, `putObjectAtBestGarrisonPoint`, `weapon->isWithinAttackRange`

### putObjectAtBestGarrisonPoint
- Purpose: Places an object at the best garrison point based on target position.
- Calls: `findClosestFreeGarrisonPointIndex`

## Globals
- **MUZZLE_FLASH_LIFETIME (Enum)**: Lifetime of muzzle flash effects.

## Dependencies
- Key includes:
  - "Common/GameState.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/Object.h"
  - "GameClient/Drawable.h"
  - "GameClient/GameClient.h"
