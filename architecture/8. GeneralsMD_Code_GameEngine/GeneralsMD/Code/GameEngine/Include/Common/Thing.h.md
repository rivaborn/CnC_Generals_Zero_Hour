# GeneralsMD/Code/GameEngine/Include/Common/Thing.h

## Purpose
Defines the base class `Thing` for game objects and drawables, holding common data and providing shared functionality.

## Responsibilities
- Provides common interface for `Object` and `Drawable` classes
- Manages spatial properties (position, orientation, transformation)
- Caches derived values (direction vectors, heights) for efficiency
- Enforces access control via protected/virtual methods

## Key Types
- **Thing (Class)**: Base class for game entities with shared spatial data
- **ThingTemplate (Class)**: Reference to template data (not defined here)
- **Object (Class)**: Logic-side representation (forward reference)
- **Drawable (Class)**: Client-side representation (forward reference)
- **Team (Class)**: Team association (forward reference)
- **AIObject (Class)**: AI-controlled entity (forward reference)
- **ThingMagicEnum (Enum)**: Not inferable (placeholder)
- **Thing_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (placeholder)
- **(anonymous enum)**: Bit flags for cache validation
  - `VALID_DIRVECTOR`: Direction vector valid
  - `VALID_ALTITUDE_TERRAIN`: Terrain height valid
  - `VALID_ALTITUDE_SEALEVEL`: Sea level height valid

## Key Functions
### `Thing(const ThingTemplate *thingTemplate)`
- Purpose: Constructor initializing template reference
- Calls: Not inferable

### `setPosition(const Coord3D *pos)`
- Purpose: Updates position and recalculates cached values
- Calls: Not inferable

### `setOrientation(Real angle)`
- Purpose: Sets orientation (aligns with Z-axis or terrain)
- Calls: Not inferable

### `calculateHeightAboveTerrain()`
- Purpose: Virtual method to compute actual height above terrain
- Calls: Not inferable
