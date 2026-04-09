# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/DumbProjectileBehavior.cpp

## Purpose
This file implements the behavior for dumb projectiles in Command & Conquer Generals, handling their launch, flight path calculation, collision detection, and detonation.

## Responsibilities
- Manage projectile launch and targeting.
- Calculate and adjust flight paths using Bezier curves.
- Handle collisions with objects and terrain.
- Detonate projectiles upon reaching target or lifespan expiration.

## Key Types
- `DumbProjectileBehaviorModuleData`: Stores configuration data for dumb projectiles.
- `DumbProjectileBehavior`: Manages the behavior of a single dumb projectile.

## Key Functions
### projectileLaunchAtObjectOrPosition
- Purpose: Prepares and launches a projectile at a target object or position.
- Calls: `Weapon::positionProjectileForLaunch`, `projectileFireAtObjectOrPosition`.

### projectileFireAtObjectOrPosition
- Purpose: Fires the projectile using a Bezier curve for flight path.
- Calls: `calcFlightPath`.

### calcFlightPath
- Purpose: Calculates the flight path of the projectile using control points and Bezier curves.
- Calls: `ThePartitionManager->estimateTerrainExtremesAlongLine`, `BezierSegment::getApproximateLength`, `BezierSegment::getSegmentPoints`.

### projectileHandleCollision
- Purpose: Handles collisions with objects, potentially detonating the projectile.
- Calls: `detonate`.

### detonate
- Purpose: Detonates the projectile, applying damage and effects.
- Calls: `TheWeaponStore->handleProjectileDetonation`, `attemptDamage`.

### update
- Purpose: Updates the projectile's position and checks for lifespan expiration or collisions.
- Calls: `detonate`.

## Globals
- `DEFAULT_MAX_LIFESPAN (Int)`: Default maximum lifespan of a dumb projectile in logic frames.

## Dependencies
- Key includes:
  - `Common/BezierSegment.h`
  - `Common/GameCommon.h`
  - `GameLogic/Object.h`
  - `GameLogic/PartitionManager.h`
  - `GameLogic/Module/DumbProjectileBehavior.h`
  - `GameLogic/Weapon.h`
