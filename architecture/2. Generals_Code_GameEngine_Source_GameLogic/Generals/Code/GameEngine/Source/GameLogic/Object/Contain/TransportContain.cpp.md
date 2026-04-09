# Generals/Code/GameEngine/Source/GameLogic/Object/Contain/TransportContain.cpp

## Purpose
This file implements the logic for transport units in Command & Conquer Generals, handling how objects can be contained within them, including capacity checks, payload creation, and exit behavior.

## Responsibilities
- Manage the containment of objects within transport units.
- Handle payload initialization and health regeneration for contained objects.
- Control the exit process of objects from transport units, including orientation and velocity transfer.
- Ensure that only allied or friendly units can be transported.

## Key Types
- **TransportContainModuleData (Struct)**: Stores configuration data for transport containment behavior.
- **TransportContain (Class)**: Manages the actual containment logic for transport units.

## Key Functions
### TransportContain::isValidContainerFor
- Purpose: Determines if an object can be contained within a transport unit, considering capacity and ownership.
- Calls:
  - `getTransportContainModuleData`
  - `OpenContain::isValidContainerFor`

### TransportContain::onContaining
- Purpose: Handles the logic when an object is added to a transport unit, including setting disabled states and updating visual conditions.
- Calls:
  - `setDisabled`
  - `getDrawable`
  - `setModelConditionState`

### TransportContain::onRemoving
- Purpose: Manages the logic when an object exits a transport unit, including position, orientation, velocity transfer, and AI behavior.
- Calls:
  - `clearDisabled`
  - `getPristineBonePositions`
  - `convertBonePosToWorldPos`
  - `setPosition`
  - `setOrientation`
  - `applyMotiveForce`
  - `setPitchRate`
  - `enableLoadSounds`
  - `addToContain`

### TransportContain::createPayload
- Purpose: Initializes the initial payload of objects within a transport unit based on configuration.
- Calls:
  - `findTemplate`
  - `newObject`
  - `isValidContainerFor`
  - `addToContain`

### TransportContain::update
- Purpose: Updates the health regeneration for contained objects and manages payload creation.
- Calls:
  - `getTransportContainModuleData`
  - `enableLoadSounds`
  - `attemptHealing`
  - `OpenContain::update`

## Globals
- None

## Dependencies
- **Includes**:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/ThingTemplate.h"
  - "Common/ThingFactory.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/AI.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/Locomotor.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/PhysicsUpdate.h"
  - "GameLogic/Module/StealthUpdate.h"
  - "GameLogic/Module/TransportContain.h"
  - "GameLogic/Object.h"

- **External Symbols**:
  - `TheGameLogic`
  - `TheThingFactory`
  - `TheAI`
