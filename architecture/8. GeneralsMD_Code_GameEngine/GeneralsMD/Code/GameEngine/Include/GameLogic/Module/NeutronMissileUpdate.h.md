# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/NeutronMissileUpdate.h

## Purpose
Defines the NeutronMissileUpdate module, handling missile behavior states and physics in the game.

## Responsibilities
- Manages missile state transitions (prelaunch, launch, attack, dead)
- Handles projectile physics (velocity, acceleration, targeting)
- Controls missile arming/detonation logic
- Manages visual effects during missile states
- Implements collision and countermeasure responses

## Key Types
- **NeutronMissileUpdateModuleData (Class)**: Contains missile configuration parameters (speeds, damping, FX references)
- **MissileStateType (Enum)**: Defines missile states (PRELAUNCH, LAUNCH, ATTACK, DEAD)
- **NeutronMissileUpdate (Class)**: Main missile behavior module implementing UpdateModule, DieModuleInterface, and ProjectileUpdateInterface

## Key Functions
### NeutronMissileUpdate::update
- Purpose: Main update loop handling state transitions and physics
- Calls: doLaunch, doAttack, detonate

### NeutronMissileUpdate::projectileLaunchAtObjectOrPosition
- Purpose: Initializes missile launch toward target
- Calls: Not inferable

### NeutronMissileUpdate::projectileFireAtObjectOrPosition
- Purpose: Fires missile at specified target
- Calls: Not inferable

### NeutronMissileUpdate::projectileHandleCollision
- Purpose: Handles collision with other objects
- Calls: Not inferable

### NeutronMissileUpdate::onDie
- Purpose: Handles missile destruction
- Calls: Not inferable

## Globals
- None

## Dependencies
- GameClient/RadiusDecal.h
- Common/GameType.h
- Common/GlobalData.h
- GameLogic/Module/UpdateModule.h
- GameLogic/Module
