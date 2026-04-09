# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/mapper.cpp - Enhanced Analysis

## Architectural Role
This file implements the texture mapping subsystem for the SAGE engine's rendering pipeline, bridging material definitions (MeshMatDescClass) with Direct3D texture stage operations. It handles both static and dynamic texture transformations, including animation and environment mapping effects.

## Cross-References
### Incoming
- **matrixmapper.cpp**: Calls `TextureMapperClass::Apply` and related methods
- **rendobj.cpp**: Uses `Reset_All_Texture_Mappers` during render object initialization
- **meshmatdesc.cpp**: Instantiates mapper classes during material loading

### Outgoing
- **dx8wrapper.h**: Directly manipulates D3D texture stage states and matrices
- **ww3d.h**: Accesses global sync time for animation timing
- **ini.h**: Reads mapper parameters from .ini files during level loading

## Design Patterns
- **Strategy Pattern**: Texture mappers implement `Apply()` with different behaviors (scale, rotate, etc.)
- **Template Method**: Base `TextureMapperClass` defines interface while derived classes implement specific transformations
- **Composite**: `CompositeTextureMapperClass` combines multiple mappers hierarchically (visible in truncated code)

*Not inferable*: Exact factory pattern usage for mapper instantiation (likely handled by MeshMatDescClass).
