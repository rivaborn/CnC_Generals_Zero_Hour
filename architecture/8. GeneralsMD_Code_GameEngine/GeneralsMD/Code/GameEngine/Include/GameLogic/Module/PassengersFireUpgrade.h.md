# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PassengersFireUpgrade.h

## Purpose
Defines an upgrade module that modifies passenger firing permissions in vehicles.

## Responsibilities
- Inherits from `UpgradeModule` to implement passenger firing logic
- Provides memory management macros for object pooling
- Exposes standard module interface methods
- Implements core upgrade behavior via `upgradeImplementation`

## Key Types
- **PassengersFireUpgrade (Class)**: Upgrade module for passenger firing permissions
- **PassengersFireUpgradeMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **PassengersFireUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### PassengersFireUpgrade()
- Purpose: Constructor for the upgrade module
- Calls: Not inferable (constructor body not shown)

### upgradeImplementation()
- Purpose: Applies the passenger firing upgrade to the target object
- Calls: Not inferable (implementation not shown)

### isSubObjectsUpgrade()
- Purpose: Indicates whether this upgrade applies to sub-objects
- Calls: None

## Globals
- None

## Dependencies
- `UpgradeModule.h` (base class)
- `Thing` (forward-declared dependency)
- Memory pool and module macro systems (internal SAGE framework)
