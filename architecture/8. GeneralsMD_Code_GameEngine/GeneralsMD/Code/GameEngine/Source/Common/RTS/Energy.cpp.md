# GeneralsMD/Code/GameEngine/Source/Common/RTS/Energy.cpp

## Purpose
Manages energy production, consumption, and power state for players in the game.

## Responsibilities
- Tracks energy production and consumption values
- Handles power sabotage effects
- Adjusts energy when objects enter/leave influence areas
- Manages power bonuses from upgrades
- Serializes energy state for save/load

## Key Types
- **Energy (Class)**: Manages player energy state and calculations
- **None**: No other classes/structs/enums defined

## Key Functions
### `getProduction`
- Purpose: Returns current energy production, accounting for sabotage
- Calls: `TheGameLogic->getFrame()`

### `getEnergySupplyRatio`
- Purpose: Calculates ratio of production to consumption
- Calls: `TheGameLogic->getFrame()`

### `hasSufficientPower`
- Purpose: Checks if production meets consumption needs
- Calls: `TheGameLogic->getFrame()`

### `adjustPower`
- Purpose: Modifies production/consumption based on power delta
- Calls: `addProduction`, `addConsumption`

### `objectEnteringInfluence`
- Purpose: Updates energy when object enters influence area
- Calls: `obj->getTemplate()->getEnergyProduction()`, `addConsumption`, `addProduction`

### `objectLeavingInfluence`
- Purpose: Updates energy when object leaves influence area
- Calls: `obj->getTemplate()->getEnergyProduction()`, `addConsumption`, `addProduction`

### `addPowerBonus`
- Purpose: Adds energy bonus from upgrades
- Calls: `obj->getTemplate()->getEnergyBonus()`, `addProduction`

### `removePowerBonus`
- Purpose: Removes energy bonus when upgrade is lost
- Calls: `obj->getTemplate()->getEnergyBonus()`, `addProduction`

### `addProduction`
- Purpose: Increases production and notifies owner
- Calls: `m_owner->onPowerBrownOutChange()`, `hasSufficientPower()`

### `addConsumption`
- Purpose: Increases consumption and notifies owner
- Calls: `m_owner->onPowerBrownOutChange()`

### `xfer`
- Purpose: Serializes energy state for save/load
- Calls: `ThePlayerList->getNthPlayer()`

## Globals
- **None**: No global/static variables

## Dependencies
- Key includes: `Common/Energy.h`, `Common/Player.h`, `Common/PlayerList.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`, `GameLogic/GameLogic.h`, `GameLogic/Object.h`
- External symbols: `TheGameLogic`, `ThePlayerList`, `XferVersion`, `XFER_SAVE`
