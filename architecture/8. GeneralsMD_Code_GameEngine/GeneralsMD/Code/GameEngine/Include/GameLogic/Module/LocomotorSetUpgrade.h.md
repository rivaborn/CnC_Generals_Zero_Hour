# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/LocomotorSetUpgrade.h

## Purpose
Defines the LocomotorSetUpgrade class, a module for upgrading a Thing's locomotion system in the game.

## Responsibilities
- Inherits from UpgradeModule to provide locomotion-specific upgrade functionality
- Manages memory allocation via custom memory pool glue macros
- Implements core upgrade behavior through upgradeImplementation
- Provides module identification and serialization macros

## Key Types
- LocomotorSetUpgrade (Class): Upgrade module for changing Thing locomotion
- LocomotorSetUpgradeMagicEnum (Enum): Not inferable (likely internal macro enum)
- LocomotorSetUpgrade_GLUE_NOT_IMPLEMENTED (Enum): Not inferable (likely internal macro enum)

## Key Functions
### LocomotorSetUpgrade()
- Purpose: Constructor for LocomotorSetUpgrade
- Calls: Not inferable

### upgradeImplementation()
- Purpose: Implements the actual locomotion upgrade logic
- Calls: Not inferable

### isSubObjectsUpgrade()
- Purpose: Indicates whether this upgrade affects sub-objects
- Calls: Not inferable

## Globals
None

## Dependencies
- UpgradeModule.h (base class)
- Thing (forward reference)
- Memory pool and module macro systems (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE, MAKE_STANDARD_MODULE_MACRO)
