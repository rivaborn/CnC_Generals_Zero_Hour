# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd8bumpdiff_constants.h - Enhanced Analysis

## Architectural Role
This header defines shader constants for DirectX 8 bump mapping and diffuse lighting, serving as the foundational configuration for the SAGE engine's rendering pipeline. It bridges the W3D subsystem's shader infrastructure with the actual shader implementations.

## Cross-References
### Incoming
- Shader implementation files (e.g., `shd8bumpdiff.cpp`) that use these constants
- W3D rendering pipeline files that set up shader registers

### Outgoing
- None (header-only, no direct calls)

## Design Patterns
- **Constant Registry Pattern**: Centralized definition of shader constants to ensure consistency across shader implementations
- **Macro-Based Configuration**: Uses preprocessor macros to define register IDs and input names for shader flexibility
- **Separation of Concerns**: Isolates shader-specific constants from the broader rendering codebase

(Word count: 150)
