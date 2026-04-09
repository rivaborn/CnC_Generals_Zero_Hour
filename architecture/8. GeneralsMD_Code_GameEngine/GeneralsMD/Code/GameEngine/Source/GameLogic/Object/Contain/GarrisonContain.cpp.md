# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/GarrisonContain.cpp

## Purpose
Manages garrison functionality for structures, handling object placement, firing positions, and containment logic.

## Responsibilities
- Manages garrison points and object placement within structures
- Handles firing positions and weapon range checks for garrisoned units
- Manages object entry/exit from garrisoned structures
- Handles damage state changes and team transitions
- Serializes/deserializes garrison state

## Key Types
- `MUZZLE_FLASH_LIFETIME` (Enum): Lifetime of muzzle flash effects in logic frames
- `GarrisonContainModuleData` (Class): Module data for garrison containment
- `GarrisonContain` (Class): Main garrison containment logic class

## Key Functions
### `calcDistSqr`
- Purpose: Calculates squared distance between two 3D coordinates
- Calls: None

### `findClosestFreeGarrisonPointIndex`
- Purpose: Finds closest available garrison point to target position
- Calls: `calcDistSqr`

### `putObjectAtGarrisonPoint`
- Purpose: Places object at specified garrison point
- Calls: `TheThingFactory->newDrawable`, `TheGameLogic->getFrame`

### `attemptBestFirePointPosition`
- Purpose: Positions object at optimal firing position and checks range
- Calls: `getObjectGarrisonPointIndex`, `putObjectAtBestGarrisonPoint`, `weapon->isWithinAttackRange`

### `onBodyDamageStateChange`
- Purpose: Handles damage state changes and orders units to exit if heavily damaged
- Calls: `orderAllPassengersToExit`

### `xfer`
- Purpose: Serializes/deserializes garrison state
- Calls: `OpenContain::xfer`, `TheTeamFactory->findTeamByID`, `TheGameLogic->findObjectByID`, `TheGameClient->findDrawableByID`

## Globals
- `MUZZLE_FLASH_LIFETIME` (const int): Muzzle flash lifetime in logic frames

## Dependencies
- Common: `GameState`, `PerfTimer`, `Player`, `PlayerList`, `Team`, `ThingFactory`, `ThingTemplate`, `Xfer`
- GameLogic: `AIPathfind`, `GameLogic`, `Object`, `AIUpdate`, `GarrisonContain`, `BodyModule`, `PartitionManager`, `Weapon`
- GameClient: `Drawable`, `GameClient`, `InGameUI`, `View`
