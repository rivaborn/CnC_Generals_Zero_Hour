# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotageCommandCenterCrateCollide.cpp

## Purpose
Handles collision logic for sabotage crates targeting command centers, resetting special power timers.

## Responsibilities
- Validates sabotage targets (enemy command centers)
- Executes sabotage effects (resets special powers)
- Triggers visual/audio feedback
- Manages serialization (CRC, Xfer)

## Key Types
- **SabotageCommandCenterCrateCollide (Class)**: Handles sabotage crate collision behavior for command centers
- **None**: No additional types defined

## Key Functions
### `isValidToExecute`
- Purpose: Checks if sabotage is valid against target object
- Calls: `CrateCollide::isValidToExecute`, `Object::isEffectivelyDead`, `Object::isKindOf`, `Object::getRelationship`

### `executeCrateBehavior`
- Purpose: Applies sabotage effects to target command center
- Calls: `TheRadar->tryInfiltrationEvent`, `doSabotageFeedbackFX`, `TheEva->setShouldPlay`, `SpecialPowerModuleInterface::startPowerRecharge`

### `crc`
- Purpose: Serialization CRC calculation
- Calls: `CrateCollide::crc`

### `xfer`
- Purpose: Serialization/deserialization
- Calls: `CrateCollide::xfer`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `CrateCollide::loadPostProcess`

## Globals
- **None**

## Dependencies
- Common: `GameAudio`, `MiscAudio`, `Player`, `PlayerList`, `Radar`, `SpecialPower`, `ThingTemplate`, `Xfer`
- GameClient: `Drawable`, `Eva`, `InGameUI`
