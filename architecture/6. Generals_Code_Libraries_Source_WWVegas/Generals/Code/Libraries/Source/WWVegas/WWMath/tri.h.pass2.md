# Generals/Code/Libraries/Source/WWVegas/WWMath/tri.h - Enhanced Analysis

## Architectural Role
This file provides core geometric primitives for collision detection, serving as a foundational layer for both game logic (e.g., unit movement) and rendering (e.g., terrain interaction). Its ray-triangle intersection logic is critical for the SAGE engine's hybrid 2D/3D rendering pipeline.

## Cross-References
### Incoming
- **Collision Detection**: Likely called by `Generals/Code/Game/Logic/Source/...` for unit-terrain interaction.
- **Rendering**: Used by `W3D` pipeline for visibility culling or LOD calculations.
- **AI Pathfinding**: May be referenced for obstacle avoidance in `Generals/Code/Game/AI/Source/...`.

### Outgoing
- **Vector Math**: Relies on `Vector2/3/4` classes for core operations.
- **Plane Math**: Uses `Vector4` for plane equations in ray-triangle tests.

## Design Patterns
- **Utility Class**: `TriClass` encapsulates triangle operations, promoting reusability.
- **Inline Functions**: Performance-critical functions (e.g., `Point_In_Triangle_2D`) are inlined to avoid call overhead.
- **Bitmask Flags**: `TRI_RAYCAST_FLAG_*` uses bitwise flags for efficient intersection result reporting.
