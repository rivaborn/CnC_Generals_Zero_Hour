# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FireOCLAfterWeaponCooldownUpdate.h

## Purpose
Manages firing an Object Creation List (OCL) after a weapon cooldown period when conditions are met.

## Responsibilities
- Tracks weapon firing status and shot counts
- Triggers OCL creation when weapon stops firing and conditions are satisfied
- Handles upgrade activation/deactivation logic via UpgradeMux
- Manages cooldown timing and shot thresholds

## Key Types
- **UpgradeMuxData (Class)**: Upgrade multiplexing data container
- **FireOCLAfterWeaponCooldownUpdateModuleData (Class)**: Module configuration data
- **FireOCLAfterWeaponCooldownUpdate (Class)**: Main module implementing OCL firing logic
- **FireOCLAfterWeaponCooldownUpdateMagicEnum (Enum)**: Not inferable
- **FireOCLAfterWeaponCooldownUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### FireOCLAfterWeaponCooldownUpdate::update
- Purpose: Called once per frame to check firing conditions
- Calls: Not inferable

### FireOCLAfterWeaponCooldownUpdate::fireOCL
- Purpose: Creates the specified OCL when conditions are met
- Calls: Not inferable

### FireOCLAfterWeaponCooldownUpdate::resetStats
- Purpose: Resets tracking statistics
- Calls: Not inferable

## Globals
- None

## Dependencies
- `UpgradeMuxData`
- `UpdateModule.h`
- `UpgradeModule.h`
- `MultiIniFieldParse`
- `ObjectCreationList`
- `Thing`
- `ModuleData`
- `UpgradeMaskType`
