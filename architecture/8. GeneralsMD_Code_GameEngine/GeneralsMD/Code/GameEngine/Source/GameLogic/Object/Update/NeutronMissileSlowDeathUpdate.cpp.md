# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/NeutronMissileSlowDeathUpdate.cpp

## Purpose
Implements the update behavior for the neutron missile superweapon's explosion sequence, handling multiple blast waves and scorch effects.

## Responsibilities
- Manages timed explosion sequences with configurable blast parameters
- Applies damage and topple effects to nearby objects
- Handles scorch mark placement and visual effects
- Serializes/deserializes state for network synchronization

## Key Types
- **NeutronMissileSlowDeathBehaviorModuleData** (Class): Contains configuration for blast parameters and effects
- **BlastInfo** (Struct): Stores individual blast wave parameters (radius, damage, timing)
- **NeutronMissileSlowDeathBehavior** (Class): Main update behavior class handling explosion logic

## Key Functions
### update
- Purpose: Main update loop that triggers blasts and scorch effects at scheduled times
- Calls: SlowDeathBehavior::update, doBlast, doScorchBlast, FXList::doFXPos

### doBlast
- Purpose: Applies damage and topple effects to objects within blast radius
- Calls: ThePartitionManager->iterateObjectsInRange, Object::topple, Object::attemptDamage, TheGameClient->addScorch

### doScorchBlast
- Purpose: Applies scorch effects to objects without causing damage
- Calls: ThePartitionManager->iterateObjectsInRange, Object::setModelConditionState

### xfer
- Purpose: Serializes/deserializes the behavior's state for network synchronization
- Calls: SlowDeathBehavior::xfer

## Globals
- None

## Dependencies
- GameLogic/Module/NeutronMissileSlowDeathUpdate.h
- GameLogic/Module/SlowDeathBehavior.h
- GameLogic/Object.h
- GameLogic/PartitionManager.h
- GameClient/FXList.h
- GameClient/GameClient.h
- Common/Xfer.h
- Common/GameState.h
- Common/Player.h
- GameLogic/TerrainLogic.h
