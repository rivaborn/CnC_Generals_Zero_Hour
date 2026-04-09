# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/ParachuteContain.cpp

## Purpose
Implements parachute behavior for transport units, including physics, bone animations, and landing logic.

## Responsibilities
- Manages parachute opening/closing and rider attachment
- Handles physics and collision for parachuting objects
- Controls bone animations for parachute and rider models
- Manages landing behavior and post-landing actions

## Key Types
- **ParachuteContainModuleData (Class)**: Contains parachute-specific configuration (pitch/roll rates, damping, etc.)
- **ParachuteContain (Class)**: Main parachute container logic
- **None**: No enums/structs defined

## Key Functions
### `update()`
- Purpose: Main update loop for parachute physics and state management
- Calls: `OpenContain::update()`, `TheTerrainLogic->getGroundHeight()`, `ThePartitionManager->findPositionAround()`, `TheAudio->addAudioEvent()`

### `onContaining(Object* rider, Bool wasSelected)`
- Purpose: Handles when an object is contained by the parachute
- Calls: `OpenContain::onContaining()`, `positionRider()`

### `onRemoving(Object* rider)`
- Purpose: Handles when an object is removed from the parachute
- Calls: `OpenContain::onRemoving()`, `TheTerrainLogic->isUnderwater()`, `TheGameLogic->findObjectByID()`

### `positionRider(Object* rider)`
- Purpose: Positions a rider relative to the parachute
- Calls: `updateBonePositions()`, `updateOffsetsFromBones()`

### `onCollide(Object* other, const Coord3D* loc, const Coord3D* normal)`
- Purpose: Handles collision events (especially ground collision)
- Calls: `removeAllContained()`

## Globals
- **NO_START_Z (Real)**: Initial Z position value (1e10)

## Dependencies
- Key includes: `PreRTS.h`, `Common/CRCDebug.h`, `GameLogic/Module/ParachuteContain.h`, `GameClient/Drawable.h`
- External symbols: `TheGameLogic`, `TheTerrainLogic`, `ThePartitionManager`, `TheAudio`, `DEBUG_CRASH`
