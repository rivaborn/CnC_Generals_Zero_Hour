# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ProjectileStreamUpdate.h

## Purpose
Manages projectile streams for visual effects, tracking projectiles to render continuous trails.

## Responsibilities
- Tracks projectile positions for stream rendering
- Manages circular buffer of projectile IDs
- Handles target changes and culling of old projectiles
- Provides position data for drawing

## Key Types
- **ProjectileStreamUpdate (Class)**: Manages projectile stream updates
- **MAX_PROJECTILE_STREAM (Enum)**: Maximum projectiles tracked (20)
- **Thing (Class)**: Forward reference to game object
- **Vector3 (Class)**: Forward reference to 3D vector
- **ProjectileStreamUpdateMagicEnum (Enum)**: Module magic number
- **ProjectileStreamUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Glue macro enum

## Key Functions
### ProjectileStreamUpdate()
- Purpose: Constructor for projectile stream tracker
- Calls: None

### addProjectile()
- Purpose: Adds a new projectile to the tracking stream
- Calls: None

### getAllPoints()
- Purpose: Retrieves all projectile positions for rendering
- Calls: None

### update()
- Purpose: Updates projectile stream state
- Calls: cullFrontOfList(), considerDying()

### cullFrontOfList()
- Purpose: Removes outdated projectiles from tracking
- Calls: None

### considerDying()
- Purpose: Determines if stream should be destroyed
- Calls: None

## Globals
- None

## Dependencies
- UpdateModule.h
- Thing (forward reference)
- Vector3 (forward reference)
- Coord3D (forward reference)
- ObjectID (forward reference)
- ModuleData (forward reference)
