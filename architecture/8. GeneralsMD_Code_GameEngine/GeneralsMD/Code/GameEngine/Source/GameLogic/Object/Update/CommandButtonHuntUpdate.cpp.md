# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/CommandButtonHuntUpdate.cpp

## Purpose
Handles "Hunting" behavior for units using special powers or commands. Activates when a unit is idle and targets appropriate enemies.

## Responsibilities
- Manages periodic scanning for valid targets based on command type
- Handles special power, weapon, and enter (hijack/sabotage/convert) hunting modes
- Prioritizes targets using distance and attack priority rules
- Integrates with AI system to control unit behavior

## Key Types
- **CommandButtonHuntUpdateModuleData (Class)**: Stores configuration (scan rate, range)
- **CommandButtonHuntUpdate (Class)**: Main update module implementing hunting logic
- **None**: No other significant types

## Key Functions
### `setCommandButton`
- Purpose: Configures the module to hunt for targets using a specific command button
- Calls: `TheControlBar->findCommandSet`, `ai->aiIdle`, `update`

### `huntSpecialPower`
- Purpose: Handles hunting for special power targets
- Calls: `ai->isIdle`, `spUpdate->isActive`, `scanClosestTarget`, `obj->doCommandButtonAtObject`

### `scanClosestTarget`
- Purpose: Finds the highest priority valid target within scan range
- Calls: `ThePartitionManager->iterateObjectsInRange`, `TheActionManager->canDoSpecialPowerAtObject`, `ThePartitionManager->getClosestObject`

### `xfer`
- Purpose: Serialization for network/savegame support
- Calls: `UpdateModule::xfer`, `xfer->xferAsciiString`, `TheControlBar->findCommandSet`

## Globals
- **None**

## Dependencies
- Key includes: `ActionManager.h`, `Player.h`, `SpecialPower.h`, `ControlBar.h`, `PartitionManager.h`, `Object.h`
- External symbols: `TheControlBar`, `ThePartitionManager`, `TheActionManager`, `TheAI`
