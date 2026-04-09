# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/DumbProjectileBehavior.cpp

## Purpose
Implements projectile behavior for missiles and shells in the game, handling trajectory calculation, collision detection, and detonation.

## Responsibilities
- Manages projectile launch, flight path calculation, and detonation
- Handles collision with targets and terrain
- Supports special behaviors like garrison clearing and flight path adjustment
- Serializes projectile state for networking

## Key Types
- `DumbProjectileBehaviorModuleData` (Class): Stores configuration for projectile behavior (lifespan, heights, tumble settings, etc.)
- `DumbProjectileBehavior` (Class): Main projectile behavior implementation
- `DEFAULT_MAX_LIFESPAN` (const Int): Default projectile lifespan in logic frames

## Key Functions
### `projectileLaunchAtObjectOrPosition`
- Purpose: Prepares projectile for launch by setting up launcher, victim, and detonation weapon
- Calls: `Weapon::positionProjectileForLaunch`, `projectileFireAtObjectOrPosition`

### `projectileFireAtObjectOrPosition`
- Purpose: Calculates and sets up the projectile's flight path
- Calls: `calcFlightPath`, `PhysicsBehavior::setPitchRate/YawRate/RollRate`

### `calcFlightPath`
- Purpose: Computes the Bezier curve flight path between start and end points
- Calls: `ThePartitionManager->estimateTerrainExtremesAlongLine`, `BezierSegment::getSegmentPoints`

### `projectileHandleCollision`
- Purpose: Handles collision with other objects, including special garrison clearing logic
- Calls: `TheGameLogic->findObjectByID`, `ContainModuleInterface` methods, `detonate`

### `detonate`
- Purpose: Triggers projectile explosion and cleanup
- Calls: `TheWeaponStore->handleProjectileDetonation`, `TheGameLogic->destroyObject`, `Object::attemptDamage`

### `update`
- Purpose: Updates projectile position and state each frame
- Calls: `detonate`, `TheTerrainLogic->getHighestLayerForDestination`, `Object::setTransformMatrix`

## Globals
- `DEFAULT_MAX_LIFESPAN` (const Int): Default projectile lifespan (10 seconds)

## Dependencies
- `BezierSegment.h`, `GameLogic.h`, `Weapon.h`, `PartitionManager.h`
- `TheGameLogic`, `ThePartitionManager`, `TheWeaponStore`, `TheTerrainLogic`
- `UpdateModule`, `PhysicsBehavior`, `ContainModuleInterface`
