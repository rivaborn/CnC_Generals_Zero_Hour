# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Object.cpp

## Purpose
Base class for game objects in the SAGE engine, handling core functionality like positioning, team management, and behavior modules.

## Responsibilities
- Manages object lifecycle (creation, updates, destruction)
- Handles team/player relationships and object status
- Coordinates behavior modules and special abilities
- Provides positioning and spatial queries
- Manages object visibility and radar representation

## Key Types
- `Object` (Class): Base class for all game objects
- `s_allWeaponFireFlags` (Enum array): Weapon fire state flags
- `BOOBY_TRAP_SCAN_RANGE` (Enum): Booby trap detection range

## Key Functions
### `addIcon`
- Purpose: Adds a visual icon at a position
- Calls: None visible

### `isPosDifferent`
- Purpose: Checks if two positions differ significantly
- Calls: None visible

### `isAngleDifferent`
- Purpose: Checks if two angles differ significantly
- Calls: None visible

### `localIsHero`
- Purpose: Determines if object is a hero unit
- Calls: None visible

### `defect`
- Purpose: Handles object team defection logic
- Calls: `cancelAndRefundAllProduction`, `tryInfiltrationEvent`, `startDefectionTimer`, `aiIdle`, `flashAsSelected`, `removeAllContained`, `defectAllParkedUnits`

### `getRadarPriority`
- Purpose: Determines object's radar display priority
- Calls: `getDefaultRadarPriority`, `isGarrisonable`, `isKindOf`

## Globals
- `s_allWeaponFireFlags` (ModelConditionFlags[3]): Predefined weapon fire state masks

## Dependencies
- Core includes: `Thing`, `ThingTemplate`, `Player`, `Team`
- Game logic: `AI`, `Weapon`, `BehaviorModule`, `PartitionManager`
- Client: `Drawable`, `ControlBar`, `Radar`
- Audio: `AudioEventRTS`, `MiscAudio`
- Common utilities: `Dict`, `BitFlagsIO`, `PerfTimer`
