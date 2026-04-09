# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/MissileAIUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the core missile behavior system, bridging the weapon firing logic (Weapon.h) with the game's AI state machine. It handles projectile physics, targeting, and detonation, serving as the runtime controller for all missile entities in the game.

## Cross-References
### Incoming
- **Weapon.cpp**: Calls `detonate()` when projectiles hit targets
- **AIUpdateInterface.cpp**: Inherits from `AIUpdateInterface`, called via `update()`
- **GameLogic.cpp**: Uses `TheGameLogic` singleton for frame timing and object destruction

### Outgoing
- **Weapon.h**: Uses `TheWeaponStore` for detonation effects and weapon templates
- **ParticleSys.h**: Manages exhaust particle systems via `TheParticleSystemManager`
- **TerrainLogic.h**: Queries terrain height for jammed missile scattering
- **StateMachine.h**: Controls missile movement via `aiMoveToPosition()`

## Design Patterns
- **State Pattern**: Missile behavior is divided into discrete states (PRELAUNCH, ATTACK, etc.) with explicit transition logic
- **Strategy Pattern**: Detonation behavior varies based on weapon template (injected via `m_detonationWeaponTmpl`)
- **Observer Pattern**: Listens for target destruction via `airborneTargetGone()` callback

*Not inferable*: Exact serialization versioning strategy for `xfer()` method.
