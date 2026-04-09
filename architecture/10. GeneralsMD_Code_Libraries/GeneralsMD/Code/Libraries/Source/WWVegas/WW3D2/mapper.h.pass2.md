# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/mapper.h - Enhanced Analysis

## Architectural Role
This file defines the texture mapping subsystem for the W3D rendering engine, providing classes that manipulate UV coordinates for various visual effects. It serves as the core interface between material definitions and the rendering pipeline, enabling dynamic texture transformations.

## Cross-References
### Incoming
- `matrixmapper.h` uses `TextureMapperClass` as a base for matrix-based mappers
- Rendering pipeline components likely instantiate and apply these mappers during material processing

### Outgoing
- Uses `INIClass` for configuration loading
- Depends on `Matrix4x4` for texture matrix calculations
- Interacts with `RenderObjClass` for object-specific mapper management

## Design Patterns
- **Factory Pattern**: `Clone()` method enables runtime creation of mapper instances
- **Strategy Pattern**: Different mapper classes implement varying UV transformation strategies
- **Composite Pattern**: Some mappers inherit from others to combine behaviors (e.g., `LinearOffsetTextureMapperClass` extending `ScaleTextureMapperClass`)
