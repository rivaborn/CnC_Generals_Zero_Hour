# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/ProjectileStreamUpdate.cpp

## Purpose
Manages a circular buffer of projectile IDs to render visual streams between firing objects and targets.

## Responsibilities
- Tracks projectile IDs in a circular buffer
- Handles target changes by inserting "holes" in the stream
- Provides projectile positions for rendering
- Cleans up invalid projectiles
- Determines when the module should be destroyed

## Key Types
- **ProjectileStreamUpdate (Class)**: Manages projectile stream rendering data
- **MAX_PROJECTILE_STREAM (const)**: Maximum number of projectiles tracked

## Key Functions
### `addProjectile`
- Purpose: Adds a new projectile ID to the stream, handling target changes
- Calls: `zero()`, `findObjectByID()`

### `cullFrontOfList`
- Purpose: Removes invalid projectile IDs from the front of the buffer
- Calls: `findObjectByID()`

### `considerDying`
- Purpose: Determines if the module should be destroyed
- Calls: `findObjectByID()`

### `getAllPoints`
- Purpose: Retrieves projectile positions for rendering
- Calls: `findObjectByID()`, `getPosition()`, `isKindOf()`, `getGeometryInfo()`

### `xfer`
- Purpose: Serializes/deserializes module state
- Calls: `UpdateModule::xfer()`

## Globals
- **m_projectileIDs (ObjectID[MAX_PROJECTILE_STREAM])**: Circular buffer of projectile IDs
- **m_owningObject (ObjectID)**: ID of the object firing projectiles
- **m_targetObject (ObjectID)**: Current target object ID
- **m_targetPosition (Coord3D)**: Current target position
- **m_nextFreeIndex (Int)**: Next available slot in buffer
- **m_firstValidIndex (Int)**: First valid projectile in buffer

## Dependencies
- `UpdateModule` (base class)
- `Xfer` (serialization)
- `GameLogic` (object management)
- `Vector3`, `Coord3D` (math types)
