# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/polyinfo.h - Enhanced Analysis

## Architectural Role
This file defines a lightweight container class (`PolygonInfoClass`) used by the W3D rendering subsystem to bundle rendering state (texture, vertex material, shader) for polygon operations. It acts as a data transfer object between rendering pipeline stages and asset management systems.

## Cross-References
### Incoming
- Rendering pipeline classes (e.g., `W3DObjectClass`, `W3DModelClass`) likely use this to store per-polygon material/shader state.
- Asset loading systems may populate `PolygonInfoClass` instances during model initialization.

### Outgoing
- Relies on `TextureClass`, `VertexMaterialClass`, and `ShaderClass` for rendering asset references.
- No direct calls to other subsystems; purely a data container.

## Design Patterns
- **Data Transfer Object (DTO)**: Encapsulates rendering state for efficient passing between subsystems.
- **Lazy Initialization**: Assets are set post-construction, allowing deferred binding.
- **Immutable Accessors**: `Peek_*` methods provide const access, enforcing read-only semantics for consumers.
