# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/WeaponSetUpgrade.h

## Purpose
Defines the WeaponSetUpgrade module, which sets weapon set bits for the Best Fit weapon set chooser.

## Responsibilities
- Inherits from UpgradeModule to provide upgrade functionality
- Implements weapon set bit manipulation for weapon selection logic
- Provides memory management via MEMORY_POOL_GLUE macros
- Exposes standard module interface via MAKE_STANDARD_MODULE_MACRO

## Key Types
- WeaponSetUpgrade (Class): Upgrade module that modifies weapon sets
- WeaponSetUpgradeMagicEnum (Enum): Not inferable (empty)
- WeaponSetUpgrade_GLUE_NOT_IMPLEMENTED (Enum): Not inferable (empty)

## Key Functions
### WeaponSetUpgrade()
- Purpose: Constructor for WeaponSetUpgrade module
- Calls: Not inferable

### upgradeImplementation()
- Purpose: Contains the actual upgrade logic implementation
- Calls: Not inferable

### isSubObjectsUpgrade()
- Purpose: Returns whether this upgrade affects sub-objects
- Calls: Not inferable

## Globals
None

## Dependencies
- UpgradeModule.h (base class)
- Thing (forward reference)
- Memory pool and module macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE, MAKE_STANDARD_MODULE_MACRO)
