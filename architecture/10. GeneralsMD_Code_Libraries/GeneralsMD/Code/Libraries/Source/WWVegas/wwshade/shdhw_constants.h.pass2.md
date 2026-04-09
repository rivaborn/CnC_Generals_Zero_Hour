# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdhw_constants.h - Enhanced Analysis

## Architectural Role
This header defines constant register indices for the SAGE engine's hardware shader system, serving as a central registry for shader parameter locations. It bridges the W3D rendering subsystem with shader implementation details, ensuring consistent parameter binding across all shader programs.

## Cross-References
### Incoming
- Shader implementation files (e.g., `shdhw_shader.cpp`) that bind parameters to these registers
- Material system files that reference lighting constants during material setup
- W3D rendering pipeline components that use these constants for shader parameter updates

### Outgoing
- None (header-only, no direct calls to other subsystems)

## Design Patterns
- **Registry Pattern**: Acts as a centralized registry for shader constant locations
- **Magic Number Replacement**: Replaces hardcoded register indices with named constants
- **Header-Only Library**: Pure declaration file with no implementation dependencies

Key insight: These constants are likely used in shader assembly code generation or parameter binding, suggesting tight coupling between this header and the shader compilation pipeline. The lighting constants (ambient/diffuse/specular) indicate this supports a 4-light model (0-3), which aligns with the engine's rendering capabilities.
