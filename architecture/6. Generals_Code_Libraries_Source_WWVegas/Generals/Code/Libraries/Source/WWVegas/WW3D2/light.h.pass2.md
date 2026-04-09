# Generals/Code/Libraries/Source/WWVegas/WW3D2/light.h - Enhanced Analysis

## Architectural Role
This file defines the core lighting abstraction in the SAGE engine's rendering pipeline. It bridges the scene graph system (via `RenderObjClass`) with the vertex processing stage, enabling dynamic lighting effects in real-time 3D rendering.

## Cross-References
### Incoming
- `SceneClass` (calls `Notify_Added`/`Notify_Removed` during scene graph operations)
- `RenderInfoClass` (used in `Render` method for vertex processing)
- `ChunkLoadClass`/`ChunkSaveClass` (for W3D asset serialization)

### Outgoing
- Inherits from `RenderObjClass` (base class for all renderable/scene graph objects)
- Uses `Vector3` for color/direction storage
- Likely interacts with `WWMath` for trigonometric calculations (spotlight angle)

## Design Patterns
- **Template Method**: `Render` is empty but marked as `virtual` - subclasses implement actual lighting logic
- **Composite**: Lights are nodes in the scene graph hierarchy (via `Notify_Added`/`Notify_Removed`)
- **Property Bag**: Encapsulates all light parameters (intensity, colors, attenuation) as member variables with getter/setter methods

*Not inferable*: Exact relationship with shadow mapping system or GPU shader binding.
