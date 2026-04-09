# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/NeutronMissileUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the missile behavior system, bridging the projectile physics engine and game logic. It implements state-driven missile behavior (launch, attack, detonation) and integrates with the broader projectile update and collision systems.

## Cross-References
### Incoming
- **Weapon systems**: Call `projectileLaunchAtObjectOrPosition` and `projectileFireAtObjectOrPosition` to initiate missile behavior.
- **Collision system**: Invokes `projectileHandleCollision` during physics updates.
- **Update loop**: Calls `update()` as part of the game's periodic module updates.

### Outgoing
- **FX system**: References `FXList` for launch/ignition effects.
- **Damage system**: Uses `DamageInfo` in `onDie()` for explosion logic.
- **Decal system**: Applies `RadiusDecal` on detonation.

## Design Patterns
- **State Pattern**: Encapsulates missile behavior states (PRELAUNCH, LAUNCH, ATTACK) with distinct transition logic.
- **Strategy Pattern**: Implements `ProjectileUpdateInterface` to decouple missile behavior from weapon systems.
- **Observer Pattern**: Notifies via `DieModuleInterface` when the missile is destroyed.
