# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StealthUpgrade.h

## Purpose
Defines a game module for applying stealth upgrades to objects.

## Responsibilities
- Inherits from `UpgradeModule` to provide stealth functionality
- Manages stealth status via `OBJECT_STATUS_CAN_STEALTH`
- Implements upgrade behavior in `upgradeImplementation()`
- Handles memory pooling and module registration

## Key Types
- **StealthUpgrade (Class)**: Module for applying stealth upgrades to objects
- **StealthUpgradeMagicEnum (Enum)**: Not inferable (likely unused placeholder)
- **StealthUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder)
- **Thing (Class)**: Forward reference to game object type

## Key Functions
### StealthUpgrade()
- Purpose: Constructor for StealthUpgrade module
- Calls: `UpgradeModule` constructor

### upgradeImplementation()
- Purpose: Applies stealth upgrade logic to the owner
- Calls: Not inferable (implementation in .cpp)

### isSubObjectsUpgrade()
- Purpose: Indicates this upgrade doesn't affect sub-objects
- Calls: None

## Globals
- None

## Dependencies
- `UpgradeModule.h` (base class)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module registration macros (`MAKE_STANDARD_MODULE_MACRO`)
- `Thing` class (forward declared)
