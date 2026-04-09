# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotageMilitaryFactoryCrateCollide.cpp

## Purpose
Handles collision behavior for sabotage crates targeting military factories in Command & Conquer Generals.

## Responsibilities
- Validates targets for sabotage (military factories only)
- Executes sabotage effects (disabling buildings)
- Manages feedback effects and EVA announcements
- Serialization/deserialization support

## Key Types
- `SabotageMilitaryFactoryCrateCollide` (Class): Manages sabotage crate collision logic
- `ModuleData` (Pointer): Configuration data for the module

## Key Functions
### `isValidToExecute`
- Purpose: Checks if target is valid for sabotage
- Calls: `CrateCollide::isValidToExecute`, `isEffectivelyDead`, `isKindOf`, `getRelationship`

### `executeCrateBehavior`
- Purpose: Applies sabotage effects to target building
- Calls: `getAIUpdateInterface`, `TheRadar->tryInfiltrationEvent`, `doSabotageFeedbackFX`, `TheEva->setShouldPlay`, `setDisabledUntil`

### `crc`
- Purpose: Serialization version control
- Calls: `CrateCollide::crc`

### `xfer`
- Purpose: Serialization implementation
- Calls: `CrateCollide::xfer`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `CrateCollide::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/GameAudio.h`, `Common/Player.h`, `Common/Radar.h`, `GameClient/Eva.h`, `GameLogic/Object.h`, `GameLogic/Module/SabotageMilitaryFactoryCrateCollide
