# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/NeutronMissileUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the core missile behavior system in the SAGE engine, acting as a specialized update module for projectile physics, targeting, and effects. It bridges the game logic layer with rendering and audio systems through its state machine and effect management.

## Cross-References
### Incoming
- **Weapon systems**: Call `projectileLaunchAtObjectOrPosition` to initiate missile launches
- **Physics system**: Invokes `projectileHandleCollision` during collision detection
- **Networking**: Uses `xfer`/`crc` for state synchronization across clients

### Outgoing
- **FX/Particle systems**: Creates visual effects via `FXList` and `ParticleSystemManager`
- **Terrain logic**: Queries `TerrainLogic` for collision responses
- **Partition manager**: Uses spatial queries for targeting calculations

## Design Patterns
- **State pattern**: Uses `MissileStateType` enum to manage launch/attack/dead states
- **Template method**: `buildFieldParse` for INI configuration parsing
- **Dependency injection**: Receives `Thing` and `ModuleData` in constructor for runtime flexibility

*Not inferable*: Exact observer relationships with UI or audio systems.
