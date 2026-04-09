# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdcubemap.cpp - Enhanced Analysis

## Architectural Role
This file implements the cube map shader system for the SAGE engine's rendering pipeline, bridging the shader definition system with Direct3D 8 hardware acceleration. It handles both the persistent definition of cube map shaders and their runtime application during rendering.

## Cross-References
### Incoming
- Shader factory system (`shddeffactory.h`) instantiates `ShdCubeMapDefClass`
- Rendering pipeline calls `Shd6CubeMapClass` methods during scene rendering
- Asset management system (`assetmgr.h`) provides texture loading via `WW3DAssetManager`

### Outgoing
- Direct3D state management through `DX8Wrapper` class
- Shader interface base class (`ShdInterfaceClass`) for common functionality
- Persistence system (`ChunkSaveClass`/`ChunkLoadClass`) for save/load operations

## Design Patterns
- **Factory Pattern**: Shader definitions are registered and instantiated through the shader factory system
- **Bridge Pattern**: Separates shader definition (`ShdCubeMapDefClass`) from its Direct3D implementation (`Shd6CubeMapClass`)
- **Resource Management**: Uses reference counting (`REF_PTR_RELEASE`) for texture cleanup

*Not inferable*: Exact vertex shader usage pattern (whether fixed-function or programmable)
