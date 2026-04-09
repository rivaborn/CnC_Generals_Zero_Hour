# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotageSupplyDropzoneCrateCollide.cpp

## Purpose
Handles collision behavior for a saboteur unit that resets timers and steals money from enemy supply dropzones.

## Responsibilities
- Validates collision targets (must be enemy supply dropzones)
- Resets dropzone timers via OCLUpdate
- Steals money from the target and awards it to the saboteur's player
- Plays audio/visual feedback (EVA messages, floating text)

## Key Types
- **SabotageSupplyDropzoneCrateCollide (Class)**: Manages sabotage behavior for supply dropzones
- **SabotageSupplyDropzoneCrateCollideModuleData (Not shown)**: Contains module-specific data (e.g., stolen cash amount)

## Key Functions
### `isValidToExecute`
- Purpose: Checks if the collision target is a valid enemy supply dropzone
- Calls: `CrateCollide::isValidToExecute`, `Object::isEffectivelyDead`, `Object::isKindOf`, `Object::getRelationship`

### `executeCrateBehavior`
- Purpose: Executes sabotage logic (timer reset, money theft, feedback)
- Calls: `TheRadar->tryInfiltrationEvent`, `doSabotageFeedbackFX`, `OCLUpdate::resetTimer`, `Money::withdraw/deposit`, `TheEva->setShouldPlay`, `TheInGameUI->addFloatingText`

### `crc` / `xfer` / `loadPostProcess`
- Purpose: Serialization and loading support (standard SAGE methods)
- Calls: Base class versions of each

## Globals
- **None**

## Dependencies
- **Includes**: `PreRTS.h`, `GameAudio.h`, `Player.h`, `Radar.h`, `ThingTemplate.h`, `Xfer.h`, `Drawable.h`, `Eva.h`, `GameText.h`, `InGameUI.h`, `ExperienceTracker.h`, `Object.h`, `PartitionManager.h`, `ScriptEngine.h`, `AIUpdate.h`, `ContainModule.h`, `DozerAIUpdate.h`, `HijackerUpdate.h`, `OCLUpdate.h`, `SabotageSupplyDropzoneCrateCollide.h`
- **External Symbols**: `TheRadar`, `TheEva`, `TheGameText`, `TheInGameUI`, `NAMEKEY`, `KINDOF_FS_SUPPLY_DROPZONE`, `EVA_CashStolen`, `EVA_BuildingSabotaged`
