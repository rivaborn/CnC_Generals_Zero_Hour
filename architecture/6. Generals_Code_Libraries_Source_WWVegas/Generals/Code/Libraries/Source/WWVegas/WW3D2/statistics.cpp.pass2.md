# Generals/Code/Libraries/Source/WWVegas/WW3D2/statistics.cpp - Enhanced Analysis

## Architectural Role
This file is the central hub for rendering performance metrics in the SAGE engine, bridging the rendering pipeline (DX8) with debugging tools. It tracks low-level GPU resource usage (textures, draw calls) and exposes this data through the `Debug_Statistics` interface, enabling both in-game debug displays and external profiling tools.

## Cross-References
### Incoming
- **DX8 Renderer**: Calls `Record_DX8_Polys_And_Vertices` and `Record_DX8_Skin_Polys_And_Vertices` during scene rendering
- **Texture System**: Invokes `Record_Texture` when textures are bound/changed
- **Frame Loop**: Initiates `Begin_Statistics`/`End_Statistics` via the game's frame timing system

### Outgoing
- **DX8Wrapper**: Delegates to `Begin_Statistics`/`End_Statistics` for wrapper-specific metrics
- **DX8Caps**: Queries `Support_NPatches()` for feature detection
- **WW3D**: Calls `Get_NPatches_Level()` for NPatch scaling calculations

## Design Patterns
- **Singleton-like**: `Debug_Statistics` acts as a global statistics collector (though not a strict singleton)
- **Frame State Pattern**: Uses `Begin_Statistics`/`End_Statistics` to encapsulate per-frame metric collection
- **Observer**: Textures and renderers "notify" this system of their usage (implicit observer pattern)
