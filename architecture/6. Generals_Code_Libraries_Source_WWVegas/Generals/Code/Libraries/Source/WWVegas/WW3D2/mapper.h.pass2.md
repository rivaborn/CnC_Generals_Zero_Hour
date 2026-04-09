# Generals/Code/Libraries/Source/WWVegas/WW3D2/mapper.h - Enhanced Analysis

## Architectural Role
This file defines the texture mapping subsystem for the W3D rendering engine, providing classes that transform UV coordinates for various visual effects. It bridges the rendering pipeline with material properties and animation systems.

## Cross-References
### Incoming
- `matrixmapper.h` references `Reset_All_Texture_Mappers` for coordinated state resets

### Outgoing
- Uses `INIClass` for configuration loading (INI parsing subsystem)
- Depends on `Vector2`/`Vector3` for coordinate math (math library)
- Integrates with `W3DMPO` (W3D object system) and `RefCountClass` (memory management)

## Design Patterns
- **Strategy Pattern**: Texture mappers implement `Apply()` with different UV transformation strategies
- **Factory Pattern**: `Clone()` method enables runtime creation of mapper instances
- **Composite Pattern**: Mappers can be chained (e.g., `LinearOffsetTextureMapperClass` extending `ScaleTextureMapperClass`)
