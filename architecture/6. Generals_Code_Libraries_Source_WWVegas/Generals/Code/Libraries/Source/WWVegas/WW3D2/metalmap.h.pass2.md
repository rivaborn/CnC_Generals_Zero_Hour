# Generals/Code/Libraries/Source/WWVegas/WW3D2/metalmap.h - Enhanced Analysis

## Architectural Role
This file defines the `MetalMapManagerClass`, which is part of the W3D rendering pipeline responsible for dynamic environment mapping. It bridges the lighting system and texture rendering, ensuring procedural metal maps update per-frame based on global lighting conditions.

## Cross-References
### Incoming
- Likely called by rendering subsystems (e.g., `WW3D2/render.cpp`) during frame updates
- Possibly referenced by material/shader systems for dynamic texture lookups

### Outgoing
- Depends on `TextureClass` for texture management
- Uses `INIClass` for configuration loading
- Relies on `Vector3` for lighting calculations

## Design Patterns
- **Singleton-like behavior**: Implied by static `_NormalTable` and global lighting state management
- **Resource Manager**: Encapsulates texture and parameter management for metal maps
- **Strategy Pattern**: Phong model parameters suggest extensibility for alternative shading models

*Not inferable*: Exact usage patterns in rendering pipeline require code inspection.
