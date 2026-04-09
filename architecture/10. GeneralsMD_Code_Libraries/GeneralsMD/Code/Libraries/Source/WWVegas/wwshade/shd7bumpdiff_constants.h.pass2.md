# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd7bumpdiff_constants.h - Enhanced Analysis

## Architectural Role
This header defines shader constants for the bump-diffuse lighting model in the SAGE engine's W3D rendering subsystem. It serves as a contract between the shader code and the rendering pipeline, ensuring consistent register and texture stage usage.

## Cross-References
### Incoming
- Shader implementation files (e.g., `shd7bumpdiff.cpp`) that use these constants
- Material system files that reference bump-diffuse shaders
- Rendering pipeline code that sets up shader constants

### Outgoing
- None (header-only, no direct calls)

## Design Patterns
- **Constant Interface Pattern**: Exposes shader constants as macros for compile-time binding
- **Register Mapping Pattern**: Defines fixed register assignments for shader inputs/outputs
- **Texture Stage Abstraction**: Isolates texture stage references (e.g., `TEX_CUBEMAP`) from implementation

Key insight: This file bridges the fixed-function pipeline (registers 1-28) and programmable shader stages, showing SAGE's hybrid rendering approach. The world/view/projection matrix layout (1-15) suggests a standardized matrix stack shared across shaders.
