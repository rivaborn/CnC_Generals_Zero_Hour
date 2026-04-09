# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/TechBuildingBehavior.cpp

## Purpose
This file implements the behavior for tech buildings in Command & Conquer Generals, handling their update cycles, capture events, and destruction.

## Responsibilities
- Manage the update cycle of tech buildings.
- Handle capture events by changing team affiliation.
- Apply visual effects (pulse FX) when captured.
- Ensure proper cleanup on destruction.

## Key Types
- TechBuildingBehaviorModuleData (struct): Stores configuration for pulse effects and rates.
- TechBuildingBehavior (class): Implements the behavior logic for tech buildings.

## Key Functions
### update
- Purpose: Updates the tech building's state, including model condition and visual effects.
- Calls:
  - `getObject()`
  - `getTechBuildingBehaviorModuleData()`
  - `setModelConditionState()`
  - `clearModelConditionState()`
  - `FXList::doFXObj()`

### onDie
- Purpose: Changes the tech building's team to neutral upon destruction.
- Calls:
  - `getObject()`
  - `setTeam()`

### onCapture
- Purpose: Wakes up the tech building for re-evaluation after a capture event.
- Calls:
  - `setWakeFrame()`

## Globals
None

## Dependencies
- Includes:
  - "PreRTS.H"
  - "Common/Player.h"
  - "Common/PlayerList.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameClient/FXList.h"
  - "GameClient/InGameUI.h"
  - "GameLogic/Module/TechBuildingBehavior.h"
  - "GameLogic/Object.h"

- External symbols:
  - `ThePlayerList`
  - `MODELCONDITION_CAPTURED`
  - `UPDATE_SLEEP_NONE`
  - `UPDATE_SLEEP_FOREVER`
