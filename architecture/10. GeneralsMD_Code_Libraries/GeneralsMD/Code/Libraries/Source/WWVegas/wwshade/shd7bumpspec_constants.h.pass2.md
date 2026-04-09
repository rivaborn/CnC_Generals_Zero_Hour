# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd7bumpspec_constants.h - Enhanced Analysis

## Architectural Role
This header defines shader constants for bump specular mapping with gloss maps, a key part of the W3D rendering pipeline. It bridges the shader assembly language with the C++ engine, enabling advanced lighting effects for 3D models.

## Cross-References
### Incoming
- Shader compilation pipeline (likely in W3D subsystem)
- Material/system definition files that reference these constants

### Outgoing
- None (header-only, defines constants used elsewhere)

## Design Patterns
- **Constant Pool Pattern**: Centralized definition of shader constants for consistency
- **Register Allocation Pattern**: Predefined register usage for shader inputs/outputs
- **Commented-Out Code**: Shows evolutionary design (unused matrix constants)

**Note**: The commented-out matrix constants suggest iterative shader development where certain transformations (world-view, inverse transpose) were experimented with but ultimately not used in the final implementation. This indicates the engine's shader system was flexible enough to support multiple lighting approaches during development.
