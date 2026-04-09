# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/WeaponBonusUpdate.h

## Purpose
Defines a game module that applies weapon bonuses to targets, similar to healing but for weapon stats.

## Responsibilities
- Manages weapon bonus application logic
- Handles target selection based on kind-of masks
- Controls bonus duration, delay, and range
- Uses condition types to define bonus effects

## Key Types
- **WeaponBonusConditionType (Enum)**: purpose not inferable.
- **WeaponBonusUpdateModuleData (Class)**: Holds configuration for bonus parameters (duration, range, etc.).
- **WeaponBonusUpdate (Class)**: Implements the update module behavior.
- **WeaponBonusUpdateMagicEnum (Enum)**: Not inferable.
- **WeaponBonusUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable.

## Key Functions
### WeaponBonusUpdateModuleData::buildFieldParse
- Purpose: Parses module data from configuration files.
- Calls: Not inferable.

### WeaponBonusUpdate::update
- Purpose: Applies weapon bonuses to eligible targets.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `UpdateModule.h` (base class)
- `MultiIniFieldParse` (for configuration parsing)
- `Thing` (game entity base class)
- `UpdateModuleData` (module data base class)
