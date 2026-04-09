# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd6bumpspec_constants.h - Enhanced Analysis

## Architectural Role
This header defines shader constants and register mappings for the SAGE engine's W3D rendering subsystem, specifically for bump specular with gloss map shaders. It serves as a central registry for shader-related constants used across vertex shaders in the rendering pipeline.

## Cross-References
### Incoming
- Vertex shader implementations in W3D subsystem (e.g., `shd6bumpspec.cpp`)
- Shader compilation/management code in W3D

### Outgoing
- None (header-only, no direct calls)

## Design Patterns
- **Constant Registry Pattern**: Centralized definition of shader constants to ensure consistency across shaders
- **Register Mapping Pattern**: Predefined register assignments for shader operations (e.g., `r0` for `HALF_ANGLE`)
- **Texture Stage Abstraction**: Separation of texture stage definitions (`TEX_CUBEMAP`) from shader logic

*Not inferable*: No clear use of other patterns like Singleton or Factory in this header.
