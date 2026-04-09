# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8caps.h - Enhanced Analysis

## Architectural Role
This file serves as the central registry for Direct3D 8 hardware capability detection, bridging the low-level graphics API with the engine's rendering pipeline. It enables feature-driven rendering paths by exposing vendor-specific quirks and shader support levels.

## Cross-References
### Incoming
- Rendering subsystem (likely `ww3d2.cpp`) queries capabilities via `Support_TnL()`, `Get_Vendor()`, etc.
- Shader manager (e.g., `shader.cpp`) checks `Get_Vertex_Shader_Major_Version()` for shader model support
- Texture system validates formats using `Support_Texture_Format()`

### Outgoing
- Directly queries `IDirect3D8` and `IDirect3DDevice8` for caps
- Uses `D3DCAPS8` for raw capability data
- Logs to `StringClass` for debugging (likely `debug.cpp`)

## Design Patterns
- **Registry Pattern**: Centralizes all capability queries through getter methods
- **Strategy Pattern**: Vendor-specific hacks (`Vendor_Specific_Hacks()`) implement different behaviors per GPU
- **Facade Pattern**: Hides Direct3D 8 complexity behind a simplified interface

*Not inferable*: Exact caller relationships without implementation analysis.
