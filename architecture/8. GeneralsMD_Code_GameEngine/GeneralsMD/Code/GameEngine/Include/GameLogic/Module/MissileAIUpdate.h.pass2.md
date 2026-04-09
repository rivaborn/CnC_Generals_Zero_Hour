# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/MissileAIUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the core missile behavior system, bridging the projectile physics system and the game's AI update framework. It implements state-driven missile logic (launch, ignition, attack) and handles targeting, collision, and detonation, making it a critical component in the weapon/attack subsystem.

## Cross-References
### Incoming
- **WeaponSystem**: Calls `projectileFireAtObjectOrPosition` to initiate missile launches
- **PhysicsSystem**: Invokes `projectileHandleCollision` for collision resolution
- **AIUpdateManager**: Uses `update()` for periodic behavior updates
- **CountermeasureSystem**: Triggers `projectileNowJammed` when decoys are deployed

### Outgoing
- **ParticleSystem**: Manages exhaust effects via `tossExhaust()`
- **WeaponTemplate**: Uses `detonationWeaponTmpl` for explosion logic
- **ObjectSystem**: References `m_launcherID` and `m_victimID` for target tracking
- **FXList**: Handles visual effects during state transitions

## Design Patterns
- **State Pattern**: Uses `MissileStateType` enum and state-specific methods (`doLaunchState`, `doAttackState`) to encapsulate different missile behaviors
- **Strategy Pattern**: `projectileFireAtObjectOrPosition` and `projectileHandleCollision` provide extensible hooks for different projectile types
- **Observer Pattern**: Listens for target destruction via `airborneTargetGone()` to adapt behavior dynamically
