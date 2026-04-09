# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/SquishCollide.cpp

## Purpose
Handles collision logic for "squish" damage when objects are crushed by larger entities.

## Responsibilities
- Detects when an object is crushed by another object (e.g., tank running over infantry)
- Applies damage to the crushed object
- Handles special cases (hijacking, TNT placement) where crushing should be ignored
- Manages serialization (CRC, Xfer) for network sync

## Key Types
- **SquishCollide (Class)**: Collision module for squish damage logic
- **DamageInfo (Struct)**: Contains damage parameters (type, amount, source)

## Key Functions
### `onCollide`
- Purpose: Processes collision events to determine if squish damage should be applied
- Calls: `getAI()`, `getGoalObject()`, `findUpdateModule()`, `findSpecialAbilityUpdate()`, `getCrusherLevel()`, `getRelationship()`, `getPhysics()`, `getGeometryInfo()`, `ThePartitionManager->geomCollidesWithGeom()`, `getPosition()`, `getOrientation()`, `getVelocity()`, `attemptDamage()`, `friend_setUndetectedDefector()`

### `crc`
- Purpose: Serialization CRC calculation
- Calls: `CollideModule::crc()`

### `xfer`
- Purpose: Serialization/deserialization handler
- Calls: `CollideModule::xfer()`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `CollideModule::loadPostProcess()`

## Globals
- **key_HijackerUpdate (NameKeyType)**: Name key for hijacker update module

## Dependencies
- `PreRTS.h`, `ThingFactory.h`, `Xfer.h`, `Damage.h`, `Object.h`, `SquishCollide.h`, `
