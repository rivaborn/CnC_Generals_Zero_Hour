# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdbumpdiff.cpp - Enhanced Analysis

## Architectural Role
This file implements the bump-diffuse shader abstraction layer, bridging between the shader definition system and hardware-specific implementations (Shd6/7/8BumpDiffClass). It handles shader version selection based on GPU capabilities and manages the shader's editable parameters.

## Cross-References
### Incoming
- **Shader Factory**: Calls `Create()` to instantiate shaders during rendering pipeline setup
- **Asset Manager**: Uses `Save()`/`Load()` for shader configuration persistence
- **Editor Tools**: Accesses editable parameters via `NAMED_EDITABLE_PARAM` macros

### Outgoing
- **Hardware Abstraction**: Queries `DX8Wrapper` for pixel shader version support
- **Shader Implementations**: Delegates to `Shd6/7/8BumpDiffClass` for version-specific initialization
- **Persistence System**: Uses `ChunkSaveClass`/`ChunkLoadClass` for serialization

## Design Patterns
- **Factory Pattern**: `Create()` method instantiates appropriate shader version
- **Strategy Pattern**: Version selection at runtime based on GPU capabilities
- **Composite Pattern**: Encapsulates both base parameters and version-specific implementations

*Not inferable*: Exact usage of `ShdVersion` class or `DECLARE_FORCE_LINK` mechanism.
