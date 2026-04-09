# Generals/Code/GameEngine/Source/GameLogic/Object/Contain/ParachuteContain.cpp

## Purpose
This file contains the implementation of the `ParachuteContain` class, which manages the behavior and logic for objects that contain other units via a parachute system in Command & Conquer Generals.

## Responsibilities
- Manage the opening and operation of parachutes.
- Handle the positioning and movement of contained units during freefall or landing.
- Ensure collision handling and status updates for both the container and contained units.
- Process AI updates, sound events, and damage calculations related to parachute operations.

## Key Types
- **ParachuteContainModuleData (struct)**: Stores configuration data for parachute behavior.
- **ParachuteContain (class)**: Manages the logic for objects containing other units via a parachute.

## Key Functions
### ParachuteContain::update
- Purpose: Updates the state of the parachute and contained units, including position, orientation, and collision handling.
- Calls:
  - `OpenContain::update()`
  - `getObject()->getPosition()`
  - `TheTerrainLogic->getGroundHeight()`
  - `parachuteAI->aiMoveToPosition()`
  - `calcSwayMtx()`
  - `positionContainedObjectsRelativeToContainer()`
  - `getObject()->kill()`

### ParachuteContain::onContaining
- Purpose: Handles the addition of a unit to the parachute container.
- Calls:
  - `OpenContain::onContaining(rider)`
  - `rider->setDisabled(DISABLED_HELD)`
  - `positionRider(rider)`

### ParachuteContain::onRemoving
- Purpose: Handles the removal of a unit from the parachute container.
- Calls:
  - `OpenContain::onRemoving(rider)`
  - `rider->clearDisabled(DISABLED_HELD)`
  - `positionRider(rider)`
  - `physics->setAllowToFall(true)`

### ParachuteContain::positionRider
- Purpose: Positions a contained unit relative to the parachute container.
- Calls:
  - `updateBonePositions()`
  - `getObject()->getPosition()`
  - `rider->setPosition(&pos)`
  - `rider->setOrientation(getObject()->getOrientation())`

## Globals
- **NO_START_Z (Real)**: A constant representing an initial Z position value.

## Dependencies
- Key includes:
  - "Common/CRCDebug.h"
  - "Common/Player.h"
  - "GameLogic/Locomotor.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/ParachuteContain.h"
  - "GameLogic/Object.h"
  - "GameClient/Drawable.h"

- External symbols used:
  - `TheGameLogic`
  - `TheTerrainLogic`
  - `TheAudio`
  - `ThePartitionManager`
