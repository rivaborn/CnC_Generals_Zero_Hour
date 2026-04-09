# GeneralsMD/Code/GameEngine/Include/Common/DrawModule.h

## Purpose
Defines the `DrawModule` base class and related interfaces for rendering objects in the game engine.

## Responsibilities
- Declares the abstract `DrawModule` class for drawable game entities
- Defines specialized interfaces for different drawable types (debris, tracers, ropes, lasers, objects)
- Provides `RenderCost` class for estimating rendering performance impact
- Declares enums for terrain decals and shadow types

## Key Types
- **DrawModule (Class)**: Abstract base class for drawable modules
- **ObjectDrawInterface (Class)**: Interface for object-specific drawing operations
- **DebrisDrawInterface (Class)**: Interface for debris drawing parameters
- **TracerDrawInterface (Class)**: Interface for tracer effects
- **RopeDrawInterface (Class)**: Interface for rope/chain rendering
- **LaserDrawInterface (Class)**: Interface for laser beam rendering
- **RenderCost (Class)**: Tracks rendering resource usage
- **TerrainDecalType (Enum)**: Types of terrain decals
- **ShadowType (Enum)**: Types of shadows

## Key Functions
### `doDrawModule`
- Purpose: Abstract method to perform actual drawing
- Calls: None visible

### `getRenderCost`
- Purpose: Estimates rendering cost (debug/internal only)
- Calls: None visible

### `reactToTransformChange`
- Purpose: Notifies module of position/rotation changes
- Calls: None visible

### `reactToGeometryChange`
- Purpose: Notifies module of geometry changes
- Calls: None visible

## Globals
- None

## Dependencies
- `Matrix3D`, `RenderCost`, `OBBoxClass` (forward declarations)
- `GameType.h`, `Module.h`, `ModelState.h`, `Color.h` (includes)
- `AsciiString`, `RGBColor`, `ModelConditionFlags` (external types)
