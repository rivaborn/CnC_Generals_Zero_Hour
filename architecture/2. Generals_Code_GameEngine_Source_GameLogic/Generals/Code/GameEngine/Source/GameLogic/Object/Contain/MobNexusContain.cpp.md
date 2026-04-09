# Generals/Code/GameEngine/Source/GameLogic/Object/Contain/MobNexusContain.cpp

## Purpose
This file implements the `MobNexusContain` module, which manages the containment and transport of units within a mob nexus in Command & Conquer Generals.

## Responsibilities
- Manages the containment logic for mob units.
- Handles the addition and removal of contained units.
- Ensures that only allied units can be contained.
- Regenerates health for contained units if configured.
- Provides functionality to evacuate contained units.

## Key Types
- `MobNexusContainModuleData (struct)`: Stores configuration data for mob nexus containment, such as slot capacity and initial payload.
- `MobNexusContain (class)`: Implements the logic for containing and managing mob units.

## Key Functions
### MobNexusContain::isValidContainerFor
- Purpose: Checks if a unit can be contained within the mob nexus.
- Calls:
  - `OpenContain::isValidContainerFor`
  - `getRelationship`
  - `getTransportSlotCount`

### MobNexusContain::onContaining
- Purpose: Handles actions when a unit is added to the mob nexus.
- Calls:
  - `setDisabled`
  - `getTransportSlotCount`
  - `getModelConditionState`
  - `setModelConditionState`

### MobNexusContain::onRemoving
- Purpose: Handles actions when a unit is removed from the mob nexus.
- Calls:
  - `clearDisabled`
  - `getPristineBonePositions`
  - `convertBonePosToWorldPos`
  - `setPosition`
  - `setOrientation`
  - `applyMotiveForce`
  - `setPitchRate`
  - `scatterToNearbyPosition`

### MobNexusContain::onObjectCreated
- Purpose: Initializes the mob nexus with its initial payload.
- Calls:
  - `findTemplate`
  - `newObject`
  - `isValidContainerFor`
  - `addToContain`

### MobNexusContain::update
- Purpose: Updates the health regeneration for contained units.
- Calls:
  - `getContainedItemsList`
  - `attemptHealing`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/ThingTemplate.h"
  - "Common/ThingFactory.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/AI.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/Locomotor.h"
  - "GameLogic/Module/StealthUpdate.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/MobNexusContain.h"
  - "GameLogic/Module/
