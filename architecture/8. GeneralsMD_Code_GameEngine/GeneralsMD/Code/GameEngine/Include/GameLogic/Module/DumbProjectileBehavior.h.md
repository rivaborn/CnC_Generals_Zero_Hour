# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DumbProjectileBehavior.h

## Purpose
Defines the `DumbProjectileBehavior` module for projectile movement and collision handling in the game.

## Responsibilities
- Manages projectile flight paths using Bezier curves
- Handles projectile collisions and detonations
- Provides projectile update interface for game logic
- Configures projectile behavior via module data

## Key Types
- **DumbProjectileBehaviorModuleData (Class)**: Stores configuration for projectile behavior (heights, lifespan, collision rules)
- **DumbProjectileBehavior (Class)**: Implements projectile movement and collision logic
- **DumbProjectileBehaviorMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **ParticleSystem (Class)**: Reference type for particle effects (external)
- **FXList (Class)**: Reference type for effects (external)

## Key Functions
### `update`
- Purpose: Updates projectile position and state each frame
- Calls: Not inferable

### `projectileLaunchAtObjectOrPosition`
- Purpose: Initializes projectile launch toward target
- Calls: `positionForLaunch`, `calcFlightPath`

### `projectileHandleCollision`
- Purpose: Handles collision with other objects
- Calls: Not inferable

### `calcFlightPath`
- Purpose: Calculates Bezier curve flight path between launcher and target
- Calls: Not inferable

## Globals
- None

## Dependencies
- `BehaviorModule.h`, `UpdateModule.h`, `CollideModule.h`
- `WeaponBonusConditionFlags.h`, `INI.h`, `Matrix3D.h`
- `ParticleSystem`, `FXList` (forward declarations)
- `MultiIniFieldParse`, `Thing`, `Object`, `WeaponTemplate`, `ParticleSystemTemplate` (external types)
