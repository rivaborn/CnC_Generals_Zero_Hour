# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/statistics.cpp - Enhanced Analysis

## Architectural Role
This file serves as the central statistics collection hub for the SAGE engine's rendering pipeline, bridging the DirectX 8 renderer (DX8Renderer) with the engine's performance monitoring system. It provides frame-level metrics that feed into both in-game debug displays and external profiling tools.

## Cross-References
### Incoming
- **DX8Renderer**: Calls `Record_DX8_Polys_And_Vertices` and `Record_DX8_Skin_Polys_And_Vertices` during scene rendering
- **WW3D**: Likely invokes `Begin_Statistics`/`End_Statistics` via the frame loop
- **Debug UI**: Accesses getter methods like `Get_Record_Texture_String()` for display

### Outgoing
- **DX8Wrapper**: Delegates to `Begin_Statistics`/`End_Statistics` for low-level stats
- **TextureLoader**: Indirectly referenced via `TextureClass` methods (e.g., `Get_Texture_Memory_Usage`)

## Design Patterns
- **Singleton-like**: `Debug_Statistics` appears to be a global monitor with no visible instantiation
- **Frame State Pattern**: Uses `Begin`/`End` pairs to demarcate statistics collection phases
- **Observer**: Passively records renderer actions without modifying them (e.g., texture changes)

*Not inferable*: Exact relationship with `DX8MeshRendererClass` (commented-out calls suggest historical coupling).
