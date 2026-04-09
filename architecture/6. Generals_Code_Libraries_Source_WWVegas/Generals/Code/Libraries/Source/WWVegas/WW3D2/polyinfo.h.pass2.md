# Generals/Code/Libraries/Source/WWVegas/WW3D2/polyinfo.h - Enhanced Analysis

## Architectural Role
This file defines a lightweight data container used by the W3D rendering pipeline to associate polygon rendering properties (texture, vertex material, shader). It acts as a bridge between high-level rendering commands and the underlying asset management system.

## Cross-References
### Incoming
- Rendering subsystems (e.g., mesh rendering, particle systems) likely use `PolygonInfoClass` to store per-polygon material/shader states.
- Animation systems may reference this for dynamic material swapping.

### Outgoing
- Relies on `TextureClass`, `VertexMaterialClass`, and `ShaderClass` for asset references (forward-declared).
- No direct calls into other subsystems; purely a data holder.

## Design Patterns
- **Data Transfer Object (DTO)**: Encapsulates rendering state for efficient passing between subsystems.
- **Lazy Initialization**: Constructor allows null pointers, deferring asset loading until needed.
- **Immutable Accessors**: `Peek_*` methods provide read-only access, enforcing encapsulation.
