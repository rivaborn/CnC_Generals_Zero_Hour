# Generals/Code/GameEngine/Source/GameLogic/Object/Contain/HealContain.cpp

## Purpose
This file implements the logic for healing objects contained within a specific type of container, ensuring that they gradually regain health over time.

## Responsibilities
- Manage the healing process for contained objects.
- Update the health status of each object in the container per frame.
- Handle the removal of fully healed objects from the container.

## Key Types
- **HealContainModuleData (struct)**: Stores data related to the healing process, such as the number of frames required for full healing.
- **HealContain (class)**: Inherits from `OpenContain` and implements the specific logic for healing contained objects.

## Key Functions
### HealContain::update
- Purpose: Updates the health status of each object in the container per frame.
- Calls:
  - OpenContain::update()
  - getHealContainModuleData()
  - doHeal()
  - reserveDoorForExit()
  - exitObjectViaDoor()

### HealContain::doHeal
- Purpose: Applies healing to a single object for one frame.
- Calls:
  - getObject()->getBodyModule()
  - attemptHealing()

## Globals
- None

## Dependencies
- **Includes**:
  - "PreRTS.h"
  - "Common/Xfer.h"
  - "GameLogic/Damage.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/HealContain.h"
  - "GameLogic/Module/UpdateModule.h"

- **External Symbols**:
  - TheGameLogic
  - DAMAGE_HEALING
  - DEATH_NONE
  - DOOR_NONE_AVAILABLE
