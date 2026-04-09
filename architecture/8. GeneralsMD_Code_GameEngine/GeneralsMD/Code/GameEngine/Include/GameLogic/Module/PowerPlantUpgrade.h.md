# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PowerPlantUpgrade.h

## Purpose
Defines the PowerPlantUpgrade module class for handling power plant upgrades in the game.

## Responsibilities
- Manages power plant upgrade logic
- Handles upgrade implementation and cleanup
- Processes capture events for upgraded objects
- Provides memory management via memory pool macros

## Key Types
- **PowerPlantUpgrade (Class)**: Module for power plant upgrades
- **PowerPlantUpgradeMagicEnum (Enum)**: Not inferable
- **PowerPlantUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### PowerPlantUpgrade()
- Purpose: Constructor for PowerPlantUpgrade
- Calls: Not inferable

### onDelete()
- Purpose: Cleanup when the module is destroyed
- Calls: Not inferable

### onCapture()
- Purpose: Handles team change events for upgraded objects
- Calls: Not inferable

### upgradeImplementation()
- Purpose: Core upgrade logic implementation
- Calls: Not inferable

### isSubObjectsUpgrade()
- Purpose: Determines if upgrade affects sub-objects
- Calls: Not inferable

## Globals
None

## Dependencies
- UpgradeModule.h
- Thing (forward reference)
- Player (forward reference)
