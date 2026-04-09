# GeneralsMD/Code/GameEngine/Include/GameClient/RayEffect.h

## Purpose
Manages ray effects (visual beams/lines) in the game world.

## Responsibilities
- Tracks ray effect data for drawables
- Adds/removes ray effects dynamically
- Provides access to ray effect data
- Maintains a fixed-size pool of ray effects

## Key Types
- **RayEffectData (struct)**: Stores drawable reference and start/end coordinates for a ray.
- **RayEffectSystem (class)**: Manages all ray effects in the game.
- **(anonymous enum)**: Defines `MAX_RAY_EFFECTS = 128`.
- **Drawable (class)**: Forward-declared reference to renderable objects.

## Key Functions
### `addRayEffect`
- Purpose: Adds a new ray effect for a drawable.
- Calls: `findEntry`

### `deleteRayEffect`
- Purpose: Removes a ray effect associated with a drawable.
- Calls: `findEntry`

### `getRayEffectData`
- Purpose: Retrieves ray effect data for a given drawable.
- Calls: `findEntry`

### `findEntry`
- Purpose: Locates a ray effect entry by its drawable.
- Calls: None

## Globals
- **TheRayEffects (RayEffectSystem*)**: Singleton instance of the ray effect system.

## Dependencies
- `Lib/BaseType.h` (for `Coord3D`)
- `Common/SubsystemInterface.h` (base class)
- `Drawable` (forward reference)
