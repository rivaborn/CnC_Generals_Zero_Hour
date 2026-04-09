# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/TempWeaponBonusHelper.h

## Purpose
Manages temporary weapon bonus effects for game objects, including application and removal.

## Responsibilities
- Apply temporary weapon bonuses to objects
- Track bonus duration and remove when expired
- Provide module interface for game logic integration

## Key Types
- **WeaponBonusConditionType (Enum)**: Not inferable.
- **TempWeaponBonusHelperModuleData (Class)**: Module data container for TempWeaponBonusHelper.
- **TempWeaponBonusHelper (Class)**: Object helper managing temporary weapon bonuses.
- **TempWeaponBonusHelperMagicEnum (Enum)**: Not inferable.
- **TempWeaponBonusHelper_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable.

## Key Functions
### TempWeaponBonusHelper()
- Purpose: Constructor for TempWeaponBonusHelper.
- Calls: Not inferable.

### getDisabledTypesToProcess()
- Purpose: Returns disabled types to process.
- Calls: Not inferable.

### update()
- Purpose: Updates the helper state, checks for bonus expiration.
- Calls: Not inferable.

### doTempWeaponBonus()
- Purpose: Applies a temporary weapon bonus with specified duration.
- Calls: Not inferable.

### clearTempWeaponBonus()
- Purpose: Removes the current temporary weapon bonus.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- **ObjectHelper.h**: Base class for object helpers.
- **WeaponBonusConditionType**: Enum used for bonus status.
