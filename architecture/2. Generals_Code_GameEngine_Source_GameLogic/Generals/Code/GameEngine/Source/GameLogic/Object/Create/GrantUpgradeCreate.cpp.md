# Generals/Code/GameEngine/Source/GameLogic/Object/Create/GrantUpgradeCreate.cpp

## Purpose
This file implements the `GrantUpgradeCreate` module, which handles granting upgrades to game objects upon creation or build completion.

## Responsibilities
- Manages upgrade grants for objects.
- Checks object status and player control.
- Handles CRC and Xfer operations for data persistence.

## Key Types
- **GrantUpgradeCreateModuleData (struct)**: Stores upgrade name and exempt status.
- **GrantUpgradeCreate (class)**: Inherits from `CreateModule` to handle specific upgrade logic.

## Key Functions
### GrantUpgradeCreate::onCreate
- Purpose: Grants an upgrade when the object is created.
- Calls:
  - `getGrantUpgradeCreateModuleData()`
  - `getObject()->getStatusBits()`
  - `TheUpgradeCenter->findUpgrade()`
  - `player->addUpgrade()`
  - `getObject()->giveUpgrade()`

### GrantUpgradeCreate::onBuildComplete
- Purpose: Grants an upgrade when the object's build is complete.
- Calls:
  - `shouldDoOnBuildComplete()`
  - `TheUpgradeCenter->findUpgrade()`
  - `player->addUpgrade()`
  - `getObject()->giveUpgrade()`

## Globals
- None

## Dependencies
- **Includes**:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/Upgrade.h"
  - "Common/Xfer.h"
  - "GameLogic/Module/GrantUpgradeCreate.h"
  - "GameLogic/Object.h"

- **External Symbols**:
  - `TheUpgradeCenter`
  - `DEBUG_ASSERTCRASH`
