# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotageFakeBuilding.cpp

## Purpose
Handles collision logic for a "saboteur" crate that destroys fake buildings when it collides with them.

## Responsibilities
- Validates collision targets (must be enemy fake buildings)
- Executes sabotage behavior (damage, effects, EVA messages)
- Manages serialization (CRC, Xfer, loadPostProcess)

## Key Types
- **SabotageFakeBuildingCrateCollide (Class)**: Manages sabotage behavior for fake buildings.
- **CrateCollide (Class)**: Base class for crate collision logic.

## Key Functions
### `isValidToExecute`
- Purpose: Checks if the target is a valid sabotage candidate (enemy fake building).
- Calls: `CrateCollide::isValidToExecute`, `other->isEffectivelyDead`, `other->isKindOf`, `getObject()->getRelationship`

### `executeCrateBehavior`
- Purpose: Applies sabotage effects (damage, radar event, EVA message) to the target.
- Calls: `TheRadar->tryInfiltrationEvent`, `doSabotageFeedbackFX`, `TheEva->setShouldPlay`, `other->attemptDamage`

### `crc`, `xfer`, `loadPostProcess`
- Purpose: Serialization methods (CRC checksum, save/load, post-load processing).
- Calls: `CrateCollide::crc`, `CrateCollide::xfer`, `CrateCollide::loadPostProcess`

## Globals
- **None**

## Dependencies
- **Includes**: `PreRTS.h`, `GameAudio.h`, `Player.h`, `Radar.h`, `ThingTemplate.h`, `Xfer.h`, `Drawable.h`, `Eva.h`, `InGame
