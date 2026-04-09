# Generals/Code/Libraries/Source/WWVegas/WW3D2/metalmap.cpp - Enhanced Analysis

## Architectural Role
This file implements the dynamic metal map generation system, which is part of the W3D rendering pipeline. It bridges the gap between static material definitions (loaded from INI) and runtime lighting calculations, enabling realistic metallic surface rendering.

## Cross-References
### Incoming
- Rendering subsystem calls `Update_Textures()` each frame to regenerate metal maps with current lighting
- Material system likely calls `Get_Metal_Map()` to retrieve textures for application to 3D models
- INI loading infrastructure calls the constructor to initialize from configuration files

### Outgoing
- Uses `VectorProcessorClass` for SIMD-optimized lighting calculations (dot products, clamping, power operations)
- Interfaces with `TextureClass` for texture management and surface locking/unlocking
- Relies on `INIClass` for configuration loading during initialization

## Design Patterns
- **Singleton-like behavior**: The `_NormalTable` static member is initialized once and shared across all instances
- **Resource Pool**: Manages an array of `TextureClass` objects that are updated dynamically
- **Strategy Pattern**: Lighting calculations can be extended by modifying the `Update_Textures()` implementation without changing callers
