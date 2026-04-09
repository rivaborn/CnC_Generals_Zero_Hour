# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpyVisionUpdate.h

## Purpose
Defines the `SpyVisionUpdate` module for handling spy vision special powers in the game.

## Responsibilities
- Manages spy vision activation/deactivation for players
- Handles upgrade logic for spy vision abilities
- Processes vision updates based on module data
- Manages disabled states (e.g., sabotage, EMP)

## Key Types
- `SpyVisionUpdateModuleData` (Class): Module data containing upgrade and spy vision settings
- `SpyVisionUpdate` (Class): Main module class implementing spy vision logic
- `SpyVisionUpdateMagicEnum` (Enum): Not inferable (likely internal macro enum)
- `SpyVisionUpdate_GLUE_NOT_IMPLEMENTED` (Enum): Not inferable (likely internal macro enum)

## Key Functions
### `SpyVisionUpdate::update`
- Purpose: Updates spy vision state each frame
- Calls: `doActivationWork`, `isUpgradeActive`, `getDisabledUntilFrame`

### `SpyVisionUpdate::activateSpyVision`
- Purpose: Activates spy vision for a specified duration
- Calls: `doActivationWork`

### `SpyVisionUpdate::upgradeImplementation`
- Purpose: Handles upgrade implementation logic
- Calls: `getUpgradeActivationMasks`, `performUpgradeFX`, `processUpgradeRemoval`

## Globals
- None

## Dependencies
- `UpdateModule.h`, `UpgradeModule.h`
- `Player` class
- `MultiIniFieldParse`, `INI` namespace
- `UpgradeMuxData`, `KindOfMaskType`
