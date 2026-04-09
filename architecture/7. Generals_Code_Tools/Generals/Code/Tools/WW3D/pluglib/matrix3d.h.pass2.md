# Generals/Code/Tools/WW3D/pluglib/matrix3d.h - Enhanced Analysis

## Architectural Role
Core mathematical foundation for 3D transformations in the SAGE engine's rendering pipeline. Provides the fundamental Matrix3D class used throughout the engine for object positioning, camera transformations, and spatial calculations.

## Cross-References
### Incoming
- Rendering subsystem (W3D) for object transformations
- Camera system for view matrix calculations
- Animation system for interpolation between keyframes
- Physics system for spatial queries

### Outgoing
- Vector math operations (vector2.h, vector3.h, vector4.h)
- Platform-specific math implementations (osdep.h)
- Other matrix classes (Matrix3, Matrix4, Quaternion)

## Design Patterns
- **Inline Implementation**: All operators and key functions are inlined for performance-critical math operations
- **Column-Vector Convention**: Uses column-vectors consistently throughout, affecting transformation order semantics
- **Implicit Last Row**: Stores only 3x4 matrix (last row always [0,0,0,1]) to optimize memory and performance

Rules followed. Output under 400 tokens.
