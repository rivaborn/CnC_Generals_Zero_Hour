# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ObjectCreationUpgrade.h

## Purpose
Defines the `ObjectCreationUpgrade` module for spawning object creation lists (OCLs) when an upgrade is applied.

## Responsibilities
- Manages upgrades that spawn objects via OCLs
- Handles module data parsing and initialization
- Implements upgrade logic and cleanup
- Provides memory management macros for the module

## Key Types
- **ObjectCreationUpgradeModuleData (Class)**: Holds OCL reference for the upgrade
- **ObjectCreationUpgrade (Class)**: Upgrade module that spawns OCLs
- **ObjectCreationUpgradeMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **ObjectCreationUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### ObjectCreationUpgradeModuleData::buildFieldParse
- Purpose: Parses module data fields from configuration files
- Calls: Not inferable

### ObjectCreationUpgrade::upgradeImplementation
- Purpose: Executes the actual upgrade logic (spawning OCL)
- Calls: Not inferable

### ObjectCreationUpgrade::onDelete
- Purpose: Cleans up resources when the module is deleted
- Calls: Not inferable

## Globals
- None

## Dependencies
- `UpgradeModule.h` (base class)
- `Thing`, `Player`, `ObjectCreationList` (forward references)
- `MultiIniFieldParse` (for field parsing)
- Memory pool and module macro utilities (internal)
