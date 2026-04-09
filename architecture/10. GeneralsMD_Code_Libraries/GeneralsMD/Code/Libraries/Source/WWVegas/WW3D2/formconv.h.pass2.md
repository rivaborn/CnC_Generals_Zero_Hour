# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/formconv.h - Enhanced Analysis

## Architectural Role
This header defines the abstraction layer between the SAGE engine's internal texture/rendering formats (WW3DFormat) and Direct3D 8's native formats (D3DFORMAT). It enables the engine to remain format-agnostic while interfacing with hardware acceleration.

## Cross-References
### Incoming
- Likely called by rendering subsystem (`ww3d2/render.cpp`) and texture loading code (`ww3d2/texture.cpp`)
- May be referenced by shader compilation or material setup code

### Outgoing
- Depends on `ww3dformat.h` for WW3D format definitions
- Uses Direct3D 8 headers (`d3d8.h`) for D3D format definitions

## Design Patterns
- **Adapter Pattern**: Bridges between WW3D and D3D format systems
- **Lookup Table**: `Init_D3D_To_WW3_Conversion` suggests precomputed conversion mappings
- **Bidirectional Conversion**: Symmetric functions for both directions (WW3D â D3D)
