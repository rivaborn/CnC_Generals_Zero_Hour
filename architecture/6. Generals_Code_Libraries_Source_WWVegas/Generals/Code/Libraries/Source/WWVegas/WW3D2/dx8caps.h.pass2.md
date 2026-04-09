# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8caps.h - Enhanced Analysis

## Architectural Role
This header defines the central capability query system for Direct3D 8 rendering in the SAGE engine. It bridges the rendering subsystem with hardware-specific feature detection, enabling conditional rendering paths based on GPU capabilities.

## Cross-References
### Incoming
- Rendering pipeline initialization (likely in `ww3d2.cpp`)
- Material/shader systems (for format/shader version checks)
- Vendor-specific driver workarounds (called by rendering initialization)

### Outgoing
- Direct3D 8 API (`IDirect3DDevice8`)
- WW3D format system (`WW3DFormat` enum)
- Rendering feature detection utilities

## Design Patterns
- **Singleton-like static class**: Centralizes capability queries without instantiation
- **Feature flag registry**: Stores capability results for runtime conditional checks
- **Vendor-specific abstraction**: Isolates driver quirks behind a dedicated method

*Not inferable: Exact caller relationships or dependency injection points.*
