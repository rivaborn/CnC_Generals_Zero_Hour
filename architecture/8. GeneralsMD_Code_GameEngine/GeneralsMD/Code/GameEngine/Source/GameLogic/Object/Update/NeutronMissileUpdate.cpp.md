# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/NeutronMissileUpdate.cpp

## Purpose
Implements missile behavior for the NeutronMissileUpdate module, handling launch, attack, and collision logic.

## Responsibilities
- Manages missile state transitions (PRELAUNCH, LAUNCH, ATTACK, DEAD)
- Handles projectile physics, targeting, and movement
- Processes collisions and detonations
- Manages visual effects (FX, particle systems, decals)
- Serializes missile state for networking

## Key Types
- **NeutronMissileUpdateModuleData (struct)**: Configuration data for missile behavior (turn rates, speeds, FX)
- **NeutronMissileUpdate (class)**: Core missile update module implementing behavior
- **MissileStateType (enum)**: State machine states (PRELAUNCH, LAUNCH, ATTACK, DEAD)

## Key Functions
### `calcTransform`
- Purpose: Calculates missile orientation toward target with turn rate constraints
- Calls: Vector3 operations (Dot_Product, Cross_Product, Normalize), Matrix3D::buildTransformMatrix

### `doLaunch`
- Purpose: Handles missile launch sequence (positioning, FX, state transition)
- Calls: FXList::doFXObj, TheParticleSystemManager->createAttachedParticleSystemID

### `doAttack`
- Purpose: Implements missile attack behavior (movement, targeting, special effects)
- Calls: calcTransform, ThePartitionManager->getDistanceSquared

### `projectileHandleCollision`
- Purpose: Processes missile collisions and detonations
- Calls: detonate, getObject()->setStatus

## Globals
- **STRAIGHT_DOWN_SLOW_FACTOR (Real)**: Factor to slow missile when descending vertically

## Dependencies
- Common: GameState, Thing, ThingTemplate, RandomValue, Xfer
- GameLogic: ExperienceTracker, GameLogic, TerrainLogic, Object, PartitionManager, AIUpdate, PhysicsUpdate
- GameClient: Drawable, FXList, InGameUI, ParticleSys
- Module-specific: NeutronMissileUpdate.h, RadiusDecalTemplate.h
