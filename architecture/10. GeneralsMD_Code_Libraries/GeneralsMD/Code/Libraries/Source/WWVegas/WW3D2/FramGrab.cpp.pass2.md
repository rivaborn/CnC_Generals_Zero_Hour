# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/FramGrab.cpp - Enhanced Analysis

## Architectural Role
This file implements frame capture functionality for video recording, bridging the rendering pipeline (WW3D2) with Windows AVI file operations. It handles format conversion and AVI stream management, serving as the engine's video recording backend.

## Cross-References
### Incoming
- Likely called from rendering or game loop systems (e.g., when recording is enabled)
- May be invoked by UI systems for replay/recording controls

### Outgoing
- Directly uses Windows AVIFile API (vfw.h) for file/stream operations
- Depends on Windows GDI for bitmap handling (GlobalAllocPtr, BITMAPINFOHEADER)
- Uses OutputDebugString for error reporting (Windows SDK)

## Design Patterns
- **Resource Acquisition Is Initialization (RAII)**: Constructor initializes AVI resources, destructor cleans them up
- **Strategy Pattern**: Different grab modes (AVI/RAW) implemented via conditional dispatch in `Grab()`
- **Data Conversion Layer**: `ConvertFrame()` acts as a transformation pipeline for color/format conversion

*Not inferable: Exact integration points with rendering pipeline or UI controls.*
