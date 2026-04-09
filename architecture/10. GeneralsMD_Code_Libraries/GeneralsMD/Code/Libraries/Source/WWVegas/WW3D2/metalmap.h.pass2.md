# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/metalmap.h - Enhanced Analysis

## Architectural Role
This file defines the `MetalMapManagerClass`, which is part of the W3D2 rendering subsystem responsible for dynamic environment mapping. It bridges the lighting system and texture rendering pipeline, enabling procedural metal map generation for realistic material shading.

## Cross-References
### Incoming
- Likely called by rendering pipeline components (e.g., material/shader systems) to fetch metal maps via `Get_Metal_Map`
- Lighting system updates metal maps through `Update_Lighting` and `Update_Textures`
- Game initialization code instantiates `MetalMapManagerClass` during engine startup

### Outgoing
- Depends on `TextureClass` for texture management (outgoing calls to texture system)
- Uses `INIClass` for configuration loading (outgoing calls to INI subsystem)
- Relies on `Vector3` for mathematical operations (outgoing calls to math library)

## Design Patterns
- **Singleton-like behavior**: Implied by static `_NormalTable` and global management role (though not strictly a singleton)
- **Resource Manager**: Encapsulates metal map textures and parameters, providing controlled access
- **Strategy Pattern**: Lighting update parameters suggest pluggable shading strategies (Phong model as current implementation)
