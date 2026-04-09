# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/MissileAIUpdate.cpp

## Purpose
Implements missile behavior logic for the game, including launch, tracking, detonation, and collision handling.

## Responsibilities
- Manages missile state transitions (prelaunch, launch, ignition, attack, kill, dead)
- Handles projectile targeting and movement
- Processes collisions and detonations
- Manages missile fuel, jamming, and countermeasure diversion

## Key Types
- `MissileAIUpdateModuleData` (Class): Stores missile configuration parameters
- `MissileAIUpdate` (Class): Main missile AI update implementation
- `MissileStateType` (Enum): Represents missile states (PRELAUNCH, LAUNCH, IGNITION, ATTACK_NOTURN, ATTACK, KILL, KILL_SELF, DEAD)

## Key Functions
### `projectileLaunchAtObjectOrPosition`
- Purpose: Prepares missile for launch toward a target
- Calls: `Weapon::positionProjectileForLaunch`, `projectileFireAtObjectOrPosition`

### `detonate`
- Purpose: Handles missile detonation logic and effects
- Calls: `TheWeaponStore->handleProjectileDetonation`, `TheGameLogic->destroyObject`

### `update`
- Purpose: Simulates one frame of missile behavior
- Calls: `doPrelaunchState`, `doLaunchState`, `doIgnitionState`, `doAttackState`, `doKillState`, `doDeadState`, `AIUpdateInterface::update`

### `projectileNowJammed`
- Purpose: Handles missile jamming behavior
- Calls: `getObject()->setModelConditionState`, `getStateMachine()->setGoalObject`, `aiMoveToPosition`

## Globals
- `BIGNUM` (Real): Large constant value (99999.0f) used for acceleration limits

## Dependencies
- Key includes: `Common/Thing.h`, `GameLogic/Module/MissileAIUpdate.h`, `GameLogic/Weapon.h`, `GameClient/ParticleSys.h`
- External symbols: `TheGameLogic`, `ThePartitionManager`, `TheTerrainLogic`, `TheWeaponStore`, `TheParticleSystemManager`
