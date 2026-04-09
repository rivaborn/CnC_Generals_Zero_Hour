# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/HiveStructureBody.cpp

## Purpose
Implements hive structure bodies that propagate damage to slave units or absorb it if no slaves are available.

## Responsibilities
- Propagates specified damage types to slave units via SpawnBehavior or ContainModule
- Absorbs damage if no slaves are available and damage type is marked for swallowing
- Falls back to parent StructureBody damage handling when propagation isn't applicable

## Key Types
- HiveStructureBodyModuleData (struct): stores damage type flags for propagation/swallowing
- HiveStructureBody (class): extends StructureBody to handle hive damage logic

## Key Functions
### HiveStructureBody::attemptDamage
- Purpose: Handles damage propagation to slaves or absorption
- Calls: getHiveStructureBodyModuleData, getObject, getDamageTypeFlag, getSpawnBehaviorInterface, getContain, getClosestSlave, getClosestRider, attemptDamage, StructureBody::attemptDamage

### HiveStructureBody::crc
- Purpose: Serialization checksum for network sync
- Calls: StructureBody::crc

### HiveStructureBody::xfer
- Purpose: Serialization method for network sync
- Calls: StructureBody::xfer

### HiveStructureBody::loadPostProcess
- Purpose: Post-load initialization
- Calls: StructureBody::loadPostProcess

## Globals
None

## Dependencies
- PreRTS.h, Common/Xfer.h, Common/ThingTemplate.h
- GameLogic/GameLogic.h, GameLogic/Object.h, GameLogic/Damage.h
- GameLogic/Module/HiveStructureBody.h, GameLogic/Module/SpawnBehavior.h, GameLogic/Module/ContainModule.h
