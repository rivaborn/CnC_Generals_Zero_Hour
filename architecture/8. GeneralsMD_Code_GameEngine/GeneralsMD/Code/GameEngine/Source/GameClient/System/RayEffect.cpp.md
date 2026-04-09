# GeneralsMD/Code/GameEngine/Source/GameClient/System/RayEffect.cpp

## Purpose
Manages ray effect system for the game, handling creation, deletion, and retrieval of ray effects tied to drawable objects.

## Responsibilities
- Maintains a list of active ray effects
- Provides methods to add, remove, and query ray effects
- Initializes and resets the ray effect system
- Tracks ray effect data (start/end positions) per drawable

## Key Types
- **RayEffectSystem (Class)**: Manages the ray effect system
- **RayEffectData (Struct)**: Stores ray effect data (drawable, start/end locations)
- **None**: No enums found

## Key Functions
### `findEntry`
- Purpose: Locates a ray effect entry by its associated drawable
- Calls: None

### `init`
- Purpose: Initializes the ray effect system by clearing all entries
- Calls: None

### `addRayEffect`
- Purpose: Adds a new ray effect for a given drawable with start/end positions
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
- `PreRTS.h`, `GameClient/RayEffect.h`, `GameClient/Drawable.h`
- Uses `Coord3D`, `Int` types from external headers
