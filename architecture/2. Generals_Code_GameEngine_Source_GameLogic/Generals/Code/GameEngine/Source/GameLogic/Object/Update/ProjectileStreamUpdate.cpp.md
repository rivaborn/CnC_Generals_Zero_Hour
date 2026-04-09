# Generals/Code/GameEngine/Source/GameLogic/Object/Update/ProjectileStreamUpdate.cpp

## Purpose
This file implements the `ProjectileStreamUpdate` class, which tracks and manages a stream of projectiles for rendering purposes in Command & Conquer Generals.

## Responsibilities
- Tracks projectile IDs in a circular array.
- Updates the draw module with projectile positions.
- Handles projectile addition and removal.
- Ensures the module dies when no valid projectiles remain and its owner is destroyed.

## Key Types
- `ProjectileStreamUpdate` (Class): Manages a stream of projectiles for rendering.

## Key Functions
### ProjectileStreamUpdate::update
- Purpose: Updates the projectile stream, culling invalid entries and checking if the module should die.
- Calls:
  - `cullFrontOfList`
  - `considerDying`
  - `TheGameLogic->destroyObject`

### ProjectileStreamUpdate::addProjectile
- Purpose: Adds a new projectile to the stream.
- Calls: None

### ProjectileStreamUpdate::cullFrontOfList
- Purpose: Removes invalid projectiles from the front of the list.
- Calls: None

### ProjectileStreamUpdate::considerDying
- Purpose: Determines if the module should be destroyed based on the state of its projectiles and owner.
- Calls:
  - `TheGameLogic->findObjectByID`

### ProjectileStreamUpdate::getAllPoints
- Purpose: Retrieves all valid projectile positions for rendering.
- Calls:
  - `TheGameLogic->findObjectByID`
  - `getPosition`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common/Xfer.h`
  - `GameLogic/GameLogic.h`
  - `GameLogic/Object.h`
  - `GameLogic/Module/ProjectileStreamUpdate.h`
  - `WWMath/Vector3.h`
