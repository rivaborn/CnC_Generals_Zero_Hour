# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/DumbProjectileBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the core projectile behavior system, bridging the weapon firing logic and physics simulation. It handles trajectory calculation, collision detection, and detonation effects, serving as the runtime controller for all projectile objects in the game.

## Cross-References
### Incoming
- Weapon systems call `projectileLaunchAtObjectOrPosition` to initiate projectiles
- Physics system references `update` for frame-by-frame movement
- Collision detection calls `projectileHandleCollision` when projectiles intersect with objects

### Outgoing
- Calls `TheWeaponStore->handleProjectileDetonation` for explosion effects
- Uses `ThePartitionManager` for terrain queries during flight path calculation
- Interfaces with `ContainModuleInterface` for garrison clearing logic
- Relies on `PhysicsBehavior` for orientation and movement

## Design Patterns
- **Strategy Pattern**: Different projectile behaviors can be configured via `DumbProjectileBehaviorModuleData` without modifying core logic
- **Observer Pattern**: Projectile state changes (detonation) trigger effects through weapon system callbacks
- **Data-Driven Design**: Flight path parameters and behaviors are loaded from INI files via `buildFieldParse`

*Not inferable*: Exact implementation of Bezier curve handling or networking synchronization details.
