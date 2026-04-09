# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/shader.h - Enhanced Analysis

## Architectural Role
This file defines the core rendering state management system for the SAGE engine's DirectX 8 backend. It encapsulates all shader-related state (blending, texturing, fog, etc.) as bit flags, providing a unified interface for rendering configuration across the engine.

## Cross-References
### Incoming
- Rendering pipeline components (e.g., `ww3d::Flush`, `DX8Wrapper`)
- Material system (`W3dMaterial3Struct`)
- Transparency sorting system (uses `StaticSortCategoryType`)

### Outgoing
- DirectX 8 state management via `DX8Wrapper` (friend class)
- String handling (`StringClass` for descriptions)
- Preset shader initialization (internal state setup)

## Design Patterns
- **Bitmask State Management**: Uses a packed unsigned integer (`ShaderBits`) to efficiently store all shader states, with bit shifts for individual property access.
- **Preset Factory**: Provides static predefined shaders for common rendering cases, reducing boilerplate code in calling systems.
- **State Caching**: Tracks global shader state (`CurrentShader`, `ShaderDirty`) to minimize DirectX state changes.

*Not inferable*: No clear use of other patterns like observer or strategy in this header.
