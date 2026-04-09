# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/MissileAIUpdate.h

## Purpose
Defines the missile behavior system for projectile AI updates in the game.

## Responsibilities
- Manages missile state transitions (prelaunch, launch, ignition, attack, etc.)
- Handles projectile targeting, collision, and detonation logic
- Controls missile fuel, speed, and exhaust effects
- Implements countermeasure diversion and jamming behavior

## Key Types
- **MissileAIUpdateModuleData (Class)**: Configuration data for missile behavior
- **MissileAIUpdate (Class)**: Core missile AI update logic
- **MissileStateType (Enum)**: Missile behavior states (PRELAUNCH, LAUNCH, IGNITION, etc.)
- **ParticleSystemID (Enum)**: Particle system identifiers
- **FXList (Class)**: Effect list reference

## Key Functions
### MissileAIUpdate::projectileFireAtObjectOrPosition
- Purpose: Initiates missile attack toward target object or position
- Calls: Not inferable

### MissileAIUpdate::projectileHandleCollision
- Purpose: Handles collision with other objects
- Calls: Not inferable

### MissileAIUpdate::update
- Purpose: Main update loop for missile behavior
- Calls: State-specific handlers (doPrelaunchState, doLaunchState, etc.)

### MissileAIUpdate::detonate
- Purpose: Handles missile detonation logic
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/GameType.h
- Common/GlobalData.h
- GameLogic/Module/AIUpdate.h
- GameLogic/WeaponBonusConditionFlags.h
- Common/INI.h
- WWMath/Matrix3D.h
