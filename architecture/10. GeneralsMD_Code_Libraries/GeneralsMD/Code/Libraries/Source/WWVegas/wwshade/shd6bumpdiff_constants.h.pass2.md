# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shd6bumpdiff_constants.h - Enhanced Analysis

## Architectural Role
This header defines shader constants for the SAGE engine's bump-diffuse rendering pipeline, specifically for vertex shader operations. It serves as a central registry for register IDs, matrix constants, and texture stage identifiers used across the rendering subsystem.

## Cross-References
### Incoming
- Shader implementation files (e.g., `shd6bumpdiff.cpp`) that use these constants
- W3D rendering pipeline code that references vertex shader inputs
- Material system files that configure shader stages

### Outgoing
- None (header-only file with no external dependencies)

## Design Patterns
- **Constant Registry Pattern**: Centralizes shader constants to ensure consistency across the rendering pipeline
- **Macro-Based Configuration**: Uses preprocessor macros for compile-time shader configuration
- **Register Allocation Pattern**: Explicitly defines register usage for vertex shader operations

Rules followed. Output under 400 tokens.
