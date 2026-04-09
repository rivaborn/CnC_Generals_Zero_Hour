# Generals/Code/Libraries/Source/WWVegas/WWMath/rect.h - Enhanced Analysis

## Architectural Role
This file defines the core 2D rectangle primitive used throughout the engine for spatial queries, UI layout, and rendering boundaries. It serves as a foundational math type that bridges geometric operations with rendering and collision systems.

## Cross-References
### Incoming
- `SurfaceRect` constructors (in `surfrect.h`) likely use `RectClass` for surface coordinate management
- `TRect<T>` template (in `trect.h`) may inherit or wrap `RectClass` for type-safe rectangle operations
- Rendering and UI systems likely depend on `Contains()` for hit-testing and visibility checks

### Outgoing
- Directly uses `Vector2` for center/extent calculations and point operations
- Relies on `MIN`/`MAX` macros for union operations (likely from a math utility header)

## Design Patterns
- **Value Object**: `RectClass` is immutable in spirit (no internal state changes except through methods), making it safe for passing/returning by value
- **Operator Overloading**: Uses `+=`, `*=`, etc. for intuitive geometric transformations (scaling, translation)
- **Composite Operations**: Methods like `Scale_Relative_Center` combine multiple transformations (translate, scale, translate back)
