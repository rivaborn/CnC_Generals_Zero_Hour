# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/FirestormDynamicGeometryInfoUpdate.cpp

## Purpose
Handles the Firestorm dynamic geometry update module, managing particle effects, damage, and scorch marks for Firestorm objects.

## Responsibilities
- Manages particle systems for Firestorm visual effects
- Applies damage to nearby objects within a radius
- Handles scorch mark placement when Firestorm reverses direction
- Updates particle system emission volumes based on Firestorm size
- Serializes/deserializes Firestorm state for networking

## Key Types
- `FirestormDynamicGeometryInfoUpdateModuleData` (Class): Stores configuration for Firestorm effects (particle systems, damage settings)
- `FirestormDynamicGeometryInfoUpdate` (Class): Implements Firestorm behavior including effects and damage
- `ParticleSystemID` (Type): Identifier for particle systems

## Key Functions
### `update`
- Purpose: Main update loop for Firestorm behavior
- Calls: `DynamicGeometryInfoUpdate::update`, `TheParticleSystemManager->createParticleSystem`, `FXList::doFXObj`, `TheGameClient->addScorch`, `doDamageScan`

### `doDamageScan`
- Purpose: Scans and damages objects within Firestorm's radius
- Calls: `ThePartitionManager->iterateObjectsInRange`, `Object::attemptDamage`

### `xfer`
- Purpose: Serializes Firestorm state for networking
- Calls: `DynamicGeometryInfoUpdate::xfer`, `Xfer::xferUser`, `Xfer::xferBool`, `Xfer::xferUnsignedInt`

## Globals
- `MAX_FIRESTORM_SYSTEMS` (const): Maximum number of particle systems (16)

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `GameClient/GameClient.h`, `GameClient/ParticleSys.h`
- `GameLogic/Damage.h`, `GameLogic/GameLogic.h`, `GameLogic/Object.h`
- `GameLogic/Module/FirestormDynamicGeometryInfoUpdate.h`
