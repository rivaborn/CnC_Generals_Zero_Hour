# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/visrasterizer.h - Enhanced Analysis

## Architectural Role
This file defines the core rasterization components for the SAGE engine's visibility system, bridging between the 3D rendering pipeline and the visibility precalculation. It handles ID buffer management and triangle rasterization in screen space, critical for occlusion culling and visibility determination.

## Cross-References
### Incoming
- **Visibility System**: Uses `VisRasterizerClass` for visibility precalculation
- **Rendering Pipeline**: Called by scene rendering code for ID buffer generation
- **Camera System**: `CameraClass` is passed to `VisRasterizerClass::Set_Camera`

### Outgoing
- **Math Library**: Uses `Matrix3D`, `Vector3` for transformations
- **Geometry System**: Works with `AABoxClass` for bounds checking
- **Memory Management**: Uses `SimpleVecClass` for temporary vertex storage

## Design Patterns
- **Composite**: `VisRasterizerClass` contains `IDBufferClass` and delegates rasterization to it
- **Strategy**: Different scanline rendering modes (occluder/non-occluder) via `Render_Mode`
- **Facade**: Provides simplified interface to complex rasterization pipeline

*Not inferable*: Exact implementation of `GradientsStruct`/`EdgeStruct` or their usage patterns.
