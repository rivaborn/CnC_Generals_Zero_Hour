# Generals/Code/GameEngine/Source/GameLogic/Object/Update/FirestormDynamicGeometryInfoUpdate.cpp - Enhanced Analysis

## Architectural Role
This file is integral to the game's dynamic geometry update system, specifically handling firestorm effects. It manages particle systems, damage scanning, and scorch marks, integrating with various subsystems like `ParticleSystemManager`, `TerrainLogic`, and `PartitionManager`.

## Cross-References
### Incoming
- **GameClient/GameClient.h**: Calls `TheGameClient->addScorch()`.
- **GameLogic/Damage.h**: Uses `DamageInfo` for damage calculations.
- **GameLogic/PartitionManager.h**: Calls `ThePartitionManager->iterateObjectsInRange()` for object scanning.

### Outgoing
- **ParticleSystemManager**: Manages particle systems through `createParticleSystem`, `findParticleSystem`, and `setEmissionVolume`.
- **TerrainLogic**: Retrieves ground height with `getGroundHeight`.
- **GameClient/FXList.h**: Handles FX operations.
- **GameLogic/Damage.h**: Applies damage to objects.

## Design Patterns
- **Observer Pattern**: The class observes changes in the game state (e.g., object positions) and reacts accordingly by updating particle systems and applying damage.
- **Strategy Pattern**: Different particle system configurations are handled through `FirestormDynamicGeometryInfoUpdateModuleData`, allowing for flexible behavior based on configuration.
- **Singleton Pattern**: Uses global instances like `TheParticleSystemManager`, `TheTerrainLogic`, and `TheGameClient` to manage shared resources.
