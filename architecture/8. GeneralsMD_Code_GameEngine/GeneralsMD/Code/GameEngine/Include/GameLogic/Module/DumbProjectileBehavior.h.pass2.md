# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DumbProjectileBehavior.h - Enhanced Analysis

## Architectural Role
This file defines the core projectile behavior module in the SAGE engine, handling movement, collision, and detonation logic for "dumb" projectiles (non-guided). It bridges the game logic layer with the physics and rendering systems through its implementation of `UpdateModule` and `ProjectileUpdateInterface`.

## Cross-References
### Incoming
- **Weapon systems**: Weapon templates call `projectileLaunchAtObjectOrPosition` to initialize projectiles
- **Collision system**: `projectileHandleCollision` is invoked by the physics/collision subsystem
- **Update loop**: Game's update system calls `update()` via `UpdateModule` interface

### Outgoing
- **Particle/FX system**: Uses `ParticleSystem` and `FXList` for visual effects
- **INI parsing**: Relies on `MultiIniFieldParse` for configuration loading
- **Math utilities**: Uses `Matrix3D` and `VecCoord3D` for flight path calculations

## Design Patterns
- **Strategy Pattern**: Implements `ProjectileUpdateInterface` to allow different projectile behaviors to be swapped
- **Data-Driven Design**: Configuration via `DumbProjectileBehaviorModuleData` loaded from INI files
- **State Machine**: Implicit state handling (launched/armed/detonated) through member variables like `m_hasDetonated`

*Not inferable*: Exact relationship with `BehaviorModule` hierarchy or memory pool management details.
