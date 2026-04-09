# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/MissileAIUpdate.cpp

## Purpose
This file implements the behavior for missile objects in the game, including their launch, tracking, and detonation logic.

## Responsibilities
- Handle missile launch and ignition.
- Manage missile state transitions (pre-launch, launch, attack, kill, dead).
- Process collisions with other objects or terrain.
- Update missile position and orientation each frame.

## Key Types
- **MissileAIUpdateModuleData (struct)**: Stores configuration data for missile behavior.
- **MissileAIUpdate (class)**: Manages the AI update logic for missile objects.

## Key Functions
### projectileLaunchAtObjectOrPosition
- Purpose: Prepares and launches a missile at a target object or position.
- Calls:
  - `Weapon::positionProjectileForLaunch`
  - `projectileFireAtObjectOrPosition`

### projectileFireAtObjectOrPosition
- Purpose: Fires the missile with specified velocity and direction.
- Calls:
  - `getObject()->getTransformMatrix()->Get_X_Vector`
  - `physics->applyMotiveForce`
  - `aiMoveToObject` or `aiMoveToPosition`

### projectileHandleCollision
- Purpose: Handles collisions between the missile and other objects or terrain.
- Calls:
  - `projectileIsArmed`
  - `TheWeaponStore->handleProjectileDetonation`
  - `FXList::doFXObj`

### detonate
- Purpose: Detonates the missile, causing damage and effects.
- Calls:
  - `TheWeaponStore->handleProjectileDetonation`
  - `getObject()->attemptDamage`
  - `TheGameLogic->destroyObject`

### update
- Purpose: Updates the missile's state each frame.
- Calls:
  - Various state-specific functions like `doPrelaunchState`, `doLaunchState`, etc.

## Globals
- **BIGNUM (Real)**: A large number used for maximum acceleration and turn rates.

## Dependencies
- Key includes:
  - "Common/Thing.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameClient/FXList.h"
  - "GameClient/ParticleSys.h"

- External symbols used:
  - `TheGameLogic`
  - `TheParticleSystemManager`
  - `TheWeaponStore`
  - `ThePartitionManager`
  - `TheTerrainLogic`
