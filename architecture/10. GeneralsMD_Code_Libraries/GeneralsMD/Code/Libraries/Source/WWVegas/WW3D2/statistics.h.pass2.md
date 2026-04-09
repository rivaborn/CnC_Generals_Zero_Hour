# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/statistics.h - Enhanced Analysis

## Architectural Role
This header defines the interface for the WW3D2 rendering statistics subsystem, which tracks GPU resource usage (textures, polygons, vertices) and draw calls. It serves as a performance monitoring layer for the DirectX8-based renderer, enabling profiling and debugging of rendering workloads.

## Cross-References
### Incoming
- Rendering pipeline components (e.g., texture managers, shader systems) likely call `Record_Texture` and `Record_DX8_Polys_And_Vertices` to log resource usage.
- Frame lifecycle managers call `Begin_Statistics`/`End_Statistics` to demarcate statistics collection periods.
- Debug UI systems may query counters like `Get_DX8_Polygons` for display.

### Outgoing
- No direct outgoing calls (header-only; implementations are in `.cpp`).
- Macros expand to `Debug_Statistics` namespace functions, implying tight coupling with the rendering backend.

## Design Patterns
- **Facade Pattern**: Exposes a simplified interface for complex rendering statistics, hiding underlying implementation details.
- **Singleton-like Behavior**: Implicit global state (e.g., texture recording mode) suggests a single statistics collector instance.
- **Macro-Based API**: Uses preprocessor macros (e.g., `DX8_RECORD_TEXTURE`) to reduce boilerplate in rendering code.
