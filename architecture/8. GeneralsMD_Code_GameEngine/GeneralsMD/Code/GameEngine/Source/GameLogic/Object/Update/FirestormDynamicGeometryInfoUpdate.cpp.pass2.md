# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/FirestormDynamicGeometryInfoUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the Firestorm ability's dynamic behavior, bridging the game logic layer with rendering and damage systems. It extends the base `DynamicGeometryInfoUpdate` to handle particle effects, area damage, and scorch marks, demonstrating how ability-specific logic is modularized in the SAGE engine.

## Cross-References
### Incoming
- **GameClient**: `TheGameClient->addScorch()` called for scorch mark placement
- **ParticleSys**: `TheParticleSystemManager->createParticleSystem()` and `findParticleSystem()` for particle effect management
- **PartitionManager**: `ThePartitionManager->iterateObjectsInRange()` for damage area scanning
- **GameLogic**: `TheGameLogic->getFrame()` for timing damage applications

### Outgoing
- **FXList**: `FXList::doFXObj()` for playing FX sequences
- **Damage**: `DamageInfo` struct for damage application
- **TerrainLogic**: `TheTerrainLogic->getGroundHeight()` for positioning effects

## Design Patterns
- **Template Method**: Extends `DynamicGeometryInfoUpdate::update()` while adding Firestorm-specific behavior
- **Object Pooling**: Uses `ParticleSystemID` to reference managed particle systems (via `TheParticleSystemManager`)
- **Strategy**: Damage application is delegated to `Object::attemptDamage()`, allowing target-specific handling

*Not inferable*: Exact serialization format for `xferUser()` or particle system lifecycle management.
