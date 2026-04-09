# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ReplaceObjectUpgrade.h

## Purpose
Defines a module for upgrading an object by replacing it with another object at the same location.

## Responsibilities
- Replace an object with a new object at the same location
- Delete the original object after replacement
- Provide module data for configuration

## Key Types
- **ReplaceObjectUpgradeModuleData (Class)**: Holds configuration data for the replacement upgrade, including the name of the replacement object.
- **ReplaceObjectUpgrade (Class)**: Implements the upgrade logic to replace an object.
- **ReplaceObjectUpgradeMagicEnum (Enum)**: Not inferable.
- **ReplaceObjectUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable.

## Key Functions
### ReplaceObjectUpgradeModuleData/buildFieldParse
- Purpose: Parses configuration data for the module.
- Calls: Not inferable.

### ReplaceObjectUpgrade/upgradeImplementation
- Purpose: Implements the actual upgrade logic to replace the object.
- Calls: Not inferable.

### ReplaceObjectUpgrade/isSubObjectsUpgrade
- Purpose: Indicates whether the upgrade applies to sub-objects.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- **UpgradeModule.h**: Base class for upgrade modules.
- **MultiIniFieldParse**: Used for parsing configuration data.
- **AsciiString**: Used for storing the replacement object name.
- **Thing**: Base class for game objects.
- **ModuleData**: Base class for module data.
- **MemoryPoolObject**: Base class for memory management.
