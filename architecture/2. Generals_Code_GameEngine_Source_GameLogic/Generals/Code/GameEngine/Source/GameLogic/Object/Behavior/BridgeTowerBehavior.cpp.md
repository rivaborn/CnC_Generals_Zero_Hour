# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/BridgeTowerBehavior.cpp

## Purpose
This file implements the behavior for bridge towers in Command & Conquer Generals, handling interactions with bridges and other towers.

## Responsibilities
- Manages damage and healing propagation between bridge towers and their associated bridge.
- Handles setting and getting of bridge IDs and tower types.
- Ensures that when a tower is damaged or healed, the same effect is applied to the bridge and other towers.

## Key Types
- `BridgeTowerBehavior` (Class): Manages behavior for bridge towers.
- `BridgeTowerType` (Enum): Represents different types of bridge towers.

## Key Functions
### BridgeTowerBehavior::onDamage
- Purpose: Handles damage received by a tower, propagating the same damage percentage to other towers and the associated bridge.
- Calls:
  - `TheGameLogic->findObjectByID`
  - `getObject()->getBodyModule()->getMaxHealth()`
  - `attemptDamage`

### BridgeTowerBehavior::onHealing
- Purpose: Handles healing received by a tower, propagating the same healing percentage to other towers and the associated bridge.
- Calls:
  - `TheGameLogic->findObjectByID`
  - `getObject()->getBodyModule()->getMaxHealth()`
  - `attemptHealing`

### BridgeTowerBehavior::onDie
- Purpose: Kills the associated bridge when a tower dies, which in turn kills all towers.
- Calls:
  - `TheGameLogic->findObjectByID`
  - `kill`

## Globals
None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameClient/InGameUI.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/BridgeBehavior.h"
  - "GameLogic/Module/BridgeTowerBehavior.h"
  - "GameLogic/TerrainLogic.h"

- External symbols used:
  - `TheGameLogic`
  - `KINDOF_BRIDGE`
  - `KINDOF_BRIDGE_TOWER`
  - `BRIDGE_MAX_TOWERS`
