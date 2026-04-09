# Generals/Code/GameEngine/Source/GameClient/System/RayEffect.cpp

## Purpose
Manages ray effect rendering in the game, tracking effects tied to drawable objects.

## Responsibilities
- Maintains a list of active ray effects
- Adds/removes ray effects for drawables
- Retrieves ray effect data for drawables
- Initializes and resets the effect system

## Key Types
- **RayEffectSystem (Class)**: Manages ray effect data and operations
- **RayEffectData (Struct)**: Stores ray effect parameters (start/end locations, drawable reference)
- **None**: No enums found

## Key Functions
### `findEntry`
- Purpose: Locates a ray effect entry by its associated drawable
- Calls: None

### `addRayEffect`
- Purpose: Adds a new ray effect for a drawable with specified start/end locations
- Calls: None

### `deleteRayEffect`
- Purpose: Removes a ray effect associated with a specific drawable
- Calls: `findEntry`

### `getRayEffectData`
- Purpose: Retrieves ray effect data for a given drawable
- Calls: `findEntry`

## Globals
- **TheRayEffects (RayEffectSystem*)**: Global instance of the ray effect system

## Dependencies
- `GameClient/RayEffect.h`
- `GameClient/Drawable.h`
- `PreRTS.h`
- `Coord3D` (assumed from game engine)
