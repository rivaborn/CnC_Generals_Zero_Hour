# Generals/Code/GameEngine/Source/GameLogic/Object/Update/FirestormDynamicGeometryInfoUpdate.cpp

## Purpose
This file implements the `FirestormDynamicGeometryInfoUpdate` class, which handles dynamic geometry updates for firestorm effects in the game. It manages particle systems, damage scanning, and scorch marks.

## Responsibilities
- Manages particle systems associated with firestorms.
- Performs damage scans to nearby objects based on a delay.
- Places scorch marks when the firestorm changes direction.
- Handles CRC and Xfer operations for data persistence.

## Key Types
- `FirestormDynamicGeometryInfoUpdateModuleData (struct)`: Stores configuration data for firestorm effects, including particle systems, FX lists, and damage parameters.
- `FirestormDynamicGeometryInfoUpdate (class)`: Manages the dynamic geometry update logic for firestorms.

## Key Functions
### FirestormDynamicGeometryInfoUpdate::update
- Purpose: Updates the firestorm's particle systems, checks for damage scanning, and places scorch marks if necessary.
- Calls:
  - `DynamicGeometryInfoUpdate::update()`
  - `TheParticleSystemManager->createParticleSystem()`
  - `ParticleSystem::setPosition()`
  - `FXList::doFXObj()`
  - `TheTerrainLogic->getGroundHeight()`
  - `ParticleSystem::setEmissionVolumeSphereRadius()`
  - `ParticleSystem::setEmissionVolumeCylinderRadius()`
  - `TheGameClient->addScorch()`
  - `doDamageScan()`

### FirestormDynamicGeometryInfoUpdate::doDamageScan
- Purpose: Scans nearby objects and applies damage based on the firestorm's configuration.
- Calls:
  - `getObject()->getGeometryInfo().getBoundingCircleRadius()`
  - `ThePartitionManager->iterateObjectsInRange()`
  - `Object::attemptDamage()`

### FirestormDynamicGeometryInfoUpdate::crc
- Purpose: Handles CRC operations for data integrity.
- Calls:
  - `DynamicGeometryInfoUpdate::crc()`

### FirestormDynamicGeometryInfoUpdate::xfer
- Purpose: Handles Xfer operations for data persistence.
- Calls:
  - `DynamicGeometryInfoUpdate::xfer()`
  - `xfer->xferUser()`
  - `xfer->xferBool()`
  - `xfer->xferUnsignedInt()`

### FirestormDynamicGeometryInfoUpdate::loadPostProcess
- Purpose: Performs post-processing after loading data.
- Calls:
  - `DynamicGeometryInfoUpdate::loadPostProcess()`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common/Xfer.h`
  - `GameClient/GameClient.h`
  - `GameClient/InGameUI.h`
  - `GameClient/FXList.h`
  - `GameClient/
