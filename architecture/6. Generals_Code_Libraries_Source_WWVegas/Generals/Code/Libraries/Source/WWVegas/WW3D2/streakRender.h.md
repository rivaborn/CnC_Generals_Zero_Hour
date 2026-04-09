# Generals/Code/Libraries/Source/WWVegas/WW3D2/streakRender.h

## Purpose
Defines the `StreakRendererClass` for low-level line rendering in the SAGE engine, used by particle and line systems.

## Responsibilities
- Manages line segment rendering properties (texture, shader, width, color, etc.)
- Handles texture mapping modes and UV animation
- Controls subdivision levels and noise for dynamic line effects
- Provides rendering methods for lines and streaks with various visual options

## Key Types
- **StreakRendererClass (Class)**: Core class for line rendering with configurable properties.
- **TextureMapMode (Enum)**: Defines texture mapping strategies (uniform width/length, tiled).
- **BitShiftOffsets (Enum)**: Bit manipulation constants for flag storage.
- **RenderInfoClass (Class)**: External rendering context (forward declared).
- **SphereClass (Class)**: External bounding volume (forward declared).
- **W3dEmitterLinePropertiesStruct (Struct)**: External properties struct (forward declared).

## Key Functions
### `Init`
- Purpose: Initializes renderer with emitter line properties.
- Calls: None visible.

### `Render`
- Purpose: Renders a line segment with given points and transform.
- Calls: `subdivision_util`.

### `RenderStreak`
- Purpose: Renders a colored, width-varying streak with personalities.
- Calls: `subdivision_util`.

### `subdivision_util`
- Purpose: Handles line subdivision for smoother rendering.
- Calls: None visible.

## Globals
- **MAX_STREAK_SUBDIV_LEVELS (const)**: Maximum subdivision level (7).

## Dependencies
- `shader.h`, `texture.h`, `matrix3d.h`, `vector2.h`
- `RenderInfoClass`, `SphereClass`, `W3dEmitterLinePropertiesStruct` (external)
