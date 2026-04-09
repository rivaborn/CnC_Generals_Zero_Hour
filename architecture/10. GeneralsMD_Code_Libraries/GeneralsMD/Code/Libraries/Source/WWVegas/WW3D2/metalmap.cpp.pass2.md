# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/metalmap.cpp - Enhanced Analysis

## Architectural Role
This file implements the dynamic metal/environment mapping system for the SAGE engine's rendering pipeline. It generates per-frame lighting textures used by 3D models to simulate metallic surfaces under varying light conditions, bridging the gap between static material properties and real-time lighting calculations.

## Cross-References
### Incoming
- **Rendering System**: Calls `Update_Textures()` during frame rendering to refresh metal maps
- **Material System**: Likely initialized via INI-based constructor when loading game assets
- **Lighting System**: Provides current lighting parameters (ambient, main light color/direction, camera direction)

### Outgoing
- **Texture System**: Creates and updates `TextureClass` objects via `TextureClass::Lock()`/`Unlock()`
- **Vector Math**: Uses `VectorProcessorClass` for optimized lighting calculations
- **INI System**: Reads material parameters during initialization

## Design Patterns
- **Resource Pool**: Manages multiple metal map textures in an array, created once and updated per-frame
- **Data-Driven Design**: Material properties loaded from INI files at runtime
- **Static Initialization**: Uses static `_NormalTable` for performance optimization (avoids per-frame recalculation)

*Not inferable*: Exact usage pattern of `REF_PTR_RELEASE` for reference counting.
