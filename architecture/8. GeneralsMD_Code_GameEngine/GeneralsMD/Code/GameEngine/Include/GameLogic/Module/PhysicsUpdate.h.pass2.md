# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PhysicsUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the core physics simulation module for rigid body dynamics in the SAGE engine. It bridges the gap between game logic (AI/direction) and rendering by managing object movement, collisions, and forces, ensuring physically plausible behavior while maintaining performance for real-time gameplay.

## Cross-References
### Incoming
- **Locomotor modules**: Call `applyForce`/`applyMotiveForce` to drive movement
- **AI modules**: Query velocity/speed via `getVelocity`/`getForwardSpeed` for pathfinding
- **Collision system**: Invokes `onCollide` for physics responses
- **Projectile system**: Uses `transferVelocityTo` during unit disgorgement

### Outgoing
- **Audio system**: Plays bounce sounds via `TheAudio`
- **Damage system**: Triggers fall damage via `m_minFallSpeedForDamage`
- **Overlap system**: Checks `checkForOverlapCollision` for continuous collision

## Design Patterns
- **Module Pattern**: Inherits from `UpdateModule` and `CollideModuleInterface` for composable behavior
- **Data-Driven Design**: Uses `PhysicsBehaviorModuleData` for configurable parameters (mass, friction, etc.)
- **Phase-Based Execution**: Runs in `PHASE_PHYSICS` to ensure deterministic order relative to AI/locomotors

*Not inferable*: Exact implementation of force accumulation or numerical integration method.
