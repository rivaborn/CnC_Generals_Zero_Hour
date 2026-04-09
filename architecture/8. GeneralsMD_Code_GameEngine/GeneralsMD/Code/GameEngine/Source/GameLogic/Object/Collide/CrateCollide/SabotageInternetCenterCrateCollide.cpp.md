# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotageInternetCenterCrateCollide.cpp

## Purpose
Handles collision behavior for a saboteur crate that temporarily disables enemy internet centers.

## Responsibilities
- Validates collision targets (must be enemy internet centers)
- Disables spy vision and hackers in the target building
- Triggers visual/audio feedback for sabotage
- Manages sabotage duration timing

## Key Types
- **SabotageInternetCenterCrateCollide (Class)**: Manages internet center sabotage logic
- **disableHacker (Function pointer)**: Callback to disable hackers in the target
- **disableInternetCenterSpyVision (Function pointer)**: Callback to disable spy vision

## Key Functions
### `isValidToExecute`
- Purpose: Checks if collision target is a valid enemy internet center
- Calls: `CrateCollide::isValidToExecute`, `Object::isEffectivelyDead`, `Object::isKindOf`, `Object::getRelationship`

### `executeCrateBehavior`
- Purpose: Executes sabotage effects on the target internet center
- Calls: `TheRadar->tryInfiltrationEvent`, `doSabotageFeedbackFX`, `TheEva->setShouldPlay`, `getControllingPlayer()->iterateObjects`, `Object::setDisabledUntil`, `ContainModuleInterface::iterateContained`

### `disableHacker`
- Purpose: Disables hackers inside the target building
- Calls: `Object::setDisabledUntil`

### `disableInternetCenterSpyVision`
- Purpose: Disables spy vision upgrades on internet centers
- Calls: `SpyVisionUpdate::setDisabledUntilFrame`

## Globals
- None

## Dependencies
- `PreRTS.h`, `GameAudio.h`, `Player.h`, `Radar.h`, `ThingTemplate.h`, `Xfer.h`
- `Drawable.h`, `Eva.h`, `GameText.h`, `InGameUI.h`
- `ExperienceTracker.h`, `Object.h`, `PartitionManager.h`, `ScriptEngine.h`
- `AIUpdate.h`, `BehaviorModule.h`, `ContainModule.h`, `DozerAIUpdate.h`, `HijackerUpdate.h`, `OCLUpdate.h`, `SabotageInternetCenterCrateCollide.h`, `SpyVisionUpdate.h`
