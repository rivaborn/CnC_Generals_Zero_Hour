# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdbumpspec.cpp - Enhanced Analysis

## Architectural Role
This file implements the bump mapping and specular shader definition class, serving as the central point for managing shader parameters, serialization, and hardware-agnostic shader version selection in the rendering pipeline.

## Cross-References
### Incoming
- Shader factory (`ShdDefFactory`) calls `Create()` to instantiate shaders
- Rendering subsystem uses `Init()`/`Shutdown()` during pipeline initialization
- Asset manager invokes `Save()`/`Load()` for shader persistence

### Outgoing
- Delegates to version-specific shaders (`Shd6BumpSpecClass`, `Shd7BumpSpecClass`, `Shd8BumpSpecClass`)
- Uses `DX8Wrapper` for hardware capability detection
- Relies on `AssetMgr` for texture loading

## Design Patterns
- **Factory Pattern**: `Create()` method acts as factory for version-specific shader instances
- **Strategy Pattern**: Runtime selection of shader implementation based on hardware capabilities
- **Composite Pattern**: Shader parameters are composed of color and texture components

*Not inferable*: Exact texture coordinate handling or bump mapping algorithm details.
