# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotageSuperweaponCrateCollide.cpp

## Purpose
Handles collision behavior for sabotage superweapon crates, which reset enemy superweapon timers.

## Responsibilities
- Validates target objects for sabotage (enemy superweapons/strategy centers)
- Executes sabotage effects (timer reset, visual/audio feedback)
- Manages EVA announcements for local player sabotage events
- Serialization/deserialization support

## Key Types
- **SabotageSuperweaponCrateCollide (Class)**: Manages sabotage crate collision logic
- **None**: No additional types defined

## Key Functions
### `isValidToExecute`
- Purpose: Checks if target is valid for sabotage (enemy superweapon/strategy center)
- Calls: `CrateCollide::isValidToExecute`, `Object::isEffectivelyDead`, `Object::isKindOf`, `Object::getRelationship`

### `executeCrateBehavior`
- Purpose: Applies sabotage effects to target object
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
- Common: `GameAudio`, `MiscAudio`, `Player`, `PlayerList`, `Radar`, `SpecialPower`, `ThingTemplate`, `
