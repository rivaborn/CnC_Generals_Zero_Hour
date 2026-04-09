# Generals/Code/GameEngine/Source/GameLogic/Object/Upgrade/PowerPlantUpgrade.cpp

## Purpose
Handles the upgrade logic for power plants in Command & Conquer Generals, including adding/removing power bonuses to players and managing capture events.

## Responsibilities
- Manages power plant upgrades.
- Handles deletion of upgraded power plants.
- Adjusts power production when a power plant is captured.
- Implements the actual upgrade process.
- Manages CRC and Xfer operations for saving/loading state.

## Key Types
- PowerPlantUpgrade (Class): Manages power plant upgrade logic.
- None

## Key Functions
### PowerPlantUpgrade
- Purpose: Constructor for PowerPlantUpgrade.
- Calls: UpgradeModule constructor.

### ~PowerPlantUpgrade
- Purpose: Destructor for PowerPlantUpgrade.
- Calls: None

### onDelete
- Purpose: Handles cleanup when the power plant is deleted.
- Calls: removePowerBonus, setUpgradeExecuted

### onCapture
- Purpose: Adjusts power bonuses when a power plant is captured.
- Calls: removePowerBonus, addPowerBonus, setUpgradeExecuted

### upgradeImplementation
- Purpose: Implements the actual upgrade of the power plant.
- Calls: addPowerBonus, extendRods

### crc
- Purpose: Handles CRC operations for saving/loading state.
- Calls: UpgradeModule::crc

### xfer
- Purpose: Handles Xfer operations for saving/loading state.
- Calls: xferVersion, UpgradeModule::xfer

### loadPostProcess
- Purpose: Re-applies power bonuses after loading a saved game.
- Calls: addPowerBonus

## Globals
- None

## Dependencies
- Key includes:
  - "Common/ModelState.h"
  - "Common/Player.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameClient/InGameUI.h"
  - "GameLogic/Object.h"
  - "
