# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/TensileFormationUpdate.cpp

## Purpose
Implements "tensile formation" movement behavior for objects, simulating springy, avalanche-like motion.

## Responsibilities
- Manages formation links between objects
- Applies physics-based movement (slope following, friction, inertia)
- Handles damage propagation and object interactions
- Controls object lifecycle (enabled/disabled states)

## Key Types
- **TensileFormationUpdate (Class)**: Main update module for tensile formation behavior
- **TensileFormationUpdateModuleData (Class)**: Module data container
- **PartitionFilterTensileFormationMember (Class)**: Filter for finding formation members
- **Link (Struct)**: Stores connection info between formation objects

## Key Functions
### `initLinks()`
- Purpose: Establishes initial connections to nearby formation members
- Calls: `ThePartitionManager->iterateObjectsInRange`, `getTFU`

### `update()`
- Purpose: Main update loop handling physics, movement, and state transitions
- Calls: `TheTerrainLogic->getGroundHeight`, `ThePartitionManager->getClosestObject`, `propagateDislodgement`

### `propagateDislodgement()`
- Purpose: Damages nearby formation members when triggered
- Calls: `ThePartitionManager->iterateObjectsInRange`, `TheGameLogic->findObjectByID`

## Globals
- **MAP_XY_FACTOR (const float)**: World space size of height map squares
- **MAP_HEIGHT_SCALE (const float)**: Height scaling factor

## Dependencies
- `UpdateModule`, `Thing`, `Object`, `PartitionFilter`
- `ThePartitionManager`, `TheTerrainLogic`, `TheGameLogic`, `TheAI`
- `AudioEventRTS`, `Drawable`, `BodyModuleInterface`
