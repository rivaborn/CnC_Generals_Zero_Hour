# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdglossmask.cpp - Enhanced Analysis

## Architectural Role
This file implements a specialized shader effect (gloss mask) within the SAGE engine's rendering pipeline. It bridges the shader definition system with DirectX 8 hardware acceleration, handling both configuration persistence and runtime rendering state management.

## Cross-References
### Incoming
- Called by shader factory system (`ShdDefFactoryClass`) during shader instantiation
- Used by rendering pipeline when applying material effects to 3D models
- Referenced by asset manager for texture loading operations

### Outgoing
- Depends on `DX8Wrapper` for all DirectX state management
- Uses `AssetMgr` for texture resource loading
- Relies on `ShdDefClass` base for persistence framework integration

## Design Patterns
- **Factory Pattern**: Shader definition registration via `REGISTER_SHDDEF`
- **Strategy Pattern**: Runtime shader implementation (`Shd6GlossMaskClass`) encapsulates DirectX-specific logic
- **Template Method**: `Apply_Shared`/`Apply_Instance` separation for shared vs. per-instance state setup

*Not inferable*: Exact vertex shader usage pattern (fixed vs. programmable pipeline)
