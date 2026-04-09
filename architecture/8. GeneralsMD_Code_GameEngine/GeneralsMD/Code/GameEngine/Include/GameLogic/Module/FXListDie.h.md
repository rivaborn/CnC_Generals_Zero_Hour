# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FXListDie.h

## Purpose
Defines the FXListDie module, which handles death effects and upgrade logic for game objects.

## Responsibilities
- Manages death effects (FXList) for objects
- Handles upgrade activation/deactivation
- Provides interface for die and upgrade modules

## Key Types
- **FXListDieModuleData (Class)**: Stores death FX and upgrade configuration
- **FXListDie (Class)**: Implements death and upgrade behavior
- **FXListDieMagicEnum (Enum)**: Not inferable (empty)
- **FXListDie_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty)

## Key Functions
### FXListDieModuleData::buildFieldParse
- Purpose: Registers INI field parsers for module data
- Calls: `DieModuleData::buildFieldParse`, `UpgradeMuxData::getFieldParse`

### FXListDie::onDie
- Purpose: Handles death effect playback
- Calls: Not inferable (body not shown)

### FXListDie::upgradeImplementation
- Purpose: Empty override for upgrade behavior
- Calls: None

## Globals
- None

## Dependencies
- `Common/INI.h`
- `GameLogic/Module/DieModule.h`
- `GameLogic/Module/UpgradeModule.h`
- `GameLogic/Weapon.h`
- `GameLogic/Damage.h`
- `Thing`, `FXList` (forward declarations)
