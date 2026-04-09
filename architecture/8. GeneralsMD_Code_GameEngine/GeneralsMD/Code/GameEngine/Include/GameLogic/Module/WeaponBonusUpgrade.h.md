# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/WeaponBonusUpgrade.h

## Purpose
Defines the WeaponBonusUpgrade module class for handling weapon upgrades in the game.

## Responsibilities
- Inherits from UpgradeModule to provide weapon-specific upgrade functionality
- Manages weapon bonus upgrades for game entities (Things)
- Implements upgrade logic through upgradeImplementation
- Provides memory management via memory pool macros

## Key Types
- **WeaponBonusUpgrade (Class)**: Main class handling weapon upgrades
- **Thing (Class)**: Forward-declared reference to game entity class
- **WeaponBonusUpgradeMagicEnum (Enum)**: Not inferable (line reference mismatch)
- **WeaponBonusUpgrade_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (line reference mismatch)

## Key Functions
### WeaponBonusUpgrade()
- Purpose: Constructor for WeaponBonusUpgrade
- Calls: Not inferable

### upgradeImplementation()
- Purpose: Implements the actual upgrade logic
- Calls: Not inferable

### isSubObjectsUpgrade()
- Purpose: Indicates whether this upgrade affects sub-objects
- Calls: Not inferable

## Globals
None

## Dependencies
- UpgradeModule.h (base class)
- Thing class (forward reference)
- Memory pool macros (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE)
- Module macros (MAKE_STANDARD_MODULE_MACRO)
