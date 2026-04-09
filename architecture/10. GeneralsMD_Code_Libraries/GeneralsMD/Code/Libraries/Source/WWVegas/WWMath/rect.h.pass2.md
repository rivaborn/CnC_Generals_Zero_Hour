# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/rect.h - Enhanced Analysis

## Architectural Role
This file defines the fundamental 2D rectangle primitive used throughout the SAGE engine for spatial queries, UI layout, and rendering operations. It serves as a foundational math utility that bridges between the rendering system (W3D) and game logic components.

## Cross-References
### Incoming
- **WWLib/surfrect.h**: Uses RectClass constructors for surface rectangle definitions
- **WWLib/trect.h**: References RectClass methods in template rectangle implementations
- **Rendering system**: Likely used for view frustum calculations and screen-space operations
- **UI system**: Used for widget positioning and hit-testing

### Outgoing
- **vector2.h**: Depends on Vector2 for coordinate operations and transformations
- **MIN/MAX macros**: Used in union operations (likely from a global math header)

## Design Patterns
- **Value Object**: RectClass is immutable in spirit (no internal state changes except through methods), making it safe for passing by value
- **Operator Overloading**: Uses +=, *=, /= for intuitive geometric transformations
- **Composite Operations**: Methods like Scale_Relative_Center combine multiple transformations atomically

**Not inferable**: No clear use of Factory, Observer, or other high-level patterns.
