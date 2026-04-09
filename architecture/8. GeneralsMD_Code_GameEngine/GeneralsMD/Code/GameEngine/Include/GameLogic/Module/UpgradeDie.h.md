# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/UpgradeDie.h

## Purpose
Defines the UpgradeDie module, which handles removal of upgrades when an object dies.

## Responsibilities
- Manages upgrade removal logic on object death
- Parses upgrade configuration from INI files
- Integrates with the game's module system

## Key Types
- **UpgradeDieModuleData (Class)**: Stores upgrade name to remove
- **UpgradeDie (Class)**: Module implementing upgrade removal on death
- **UpgradeDieMagicEnum (Enum)**: Not inferable
- **UpgradeDie_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### UpgradeDieModuleData::buildFieldParse
- Purpose: Registers INI field parsing for upgrade name
- Calls: DieModuleData::buildFieldParse

### UpgradeDie::onDie
- Purpose: Handles upgrade removal when object dies
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/INI.h
- GameLogic/Module/DieModule.h
- Thing (forward reference)
