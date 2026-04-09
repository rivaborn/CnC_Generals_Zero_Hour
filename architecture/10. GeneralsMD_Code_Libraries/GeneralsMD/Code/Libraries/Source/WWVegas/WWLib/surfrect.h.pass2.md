# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/surfrect.h - Enhanced Analysis

## Architectural Role
This header defines a utility class (`SurfaceRect`) used in the rendering subsystem to associate a surface with a clipping rectangle and a 2D coordinate. It serves as a convenience wrapper for operations requiring both surface access and clipping logic, likely used in the W3D rendering pipeline.

## Cross-References
### Incoming
- Rendering-related modules (e.g., W3D rendering code) that need to perform clipped surface operations.
- UI rendering code that requires surface clipping for widgets or HUD elements.

### Outgoing
- **surface.h**: Uses `Surface` class and its `Get_Rect()` method.
- **trect.h**: Uses `Rect` for clipping window definition.
- **point.h**: Uses `Point2D` for coordinate tracking.

## Design Patterns
- **Wrapper/Adapter Pattern**: `SurfaceRect` adapts a `Surface` with additional clipping and coordinate data, simplifying rendering operations.
- **Immutable Design**: Copy constructor and assignment operator are explicitly deleted to enforce immutability, preventing accidental modifications.
- **Not inferable**: No other patterns are clearly evident from the header alone.
