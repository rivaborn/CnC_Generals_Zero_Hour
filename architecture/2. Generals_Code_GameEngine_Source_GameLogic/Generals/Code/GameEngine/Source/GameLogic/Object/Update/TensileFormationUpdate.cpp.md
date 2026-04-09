# Generals/Code/GameEngine/Source/GameLogic/Object/Update/TensileFormationUpdate.cpp

## Purpose
This file implements the `TensileFormationUpdate` class, which handles the springy formation movement behavior for objects in Command & Conquer Generals.

## Responsibilities
- Manages tensile formation updates.
- Initializes and maintains links between formation members.
- Applies physics and tensor calculations to simulate movement.
- Propagates dislodgement effects within the formation.

## Key Types
- **PartitionFilterTensileFormationMember (Class)**: Filters objects for tensile formation membership.

## Key Functions
### getTFU
- Purpose: Retrieves the `TensileFormationUpdate` module from an object.
- Calls: `findUpdateModule`

### TensileFormationUpdate::initLinks
- Purpose: Initializes links between formation members.
- Calls: `iterateObjectsInRange`, `setOrientation`

### TensileFormationUpdate::update
- Purpose: Updates the tensile formation's state and movement.
- Calls: `getGroundHeight`, `addAudioEvent`, `findObjectByID`, `setPosition`

### TensileFormationUpdate::propagateDislodgement
- Purpose: Propagates dislodgement effects to other formation members.
- Calls: `iterateObjectsInRange`, `setDamageState`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/Xfer.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/TensileFormationUpdate.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/AIPathfind.h"
