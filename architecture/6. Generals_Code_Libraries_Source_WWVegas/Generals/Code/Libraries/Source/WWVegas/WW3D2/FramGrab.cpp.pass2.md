# Generals/Code/Libraries/Source/WWVegas/WW3D2/FramGrab.cpp - Enhanced Analysis

## Architectural Role
This file implements the video recording subsystem in the SAGE engine, specifically handling AVI file creation and frame capture. It bridges the rendering pipeline with Windows AVI APIs, enabling replay/debug functionality.

## Cross-References
### Incoming
- Likely called from rendering/debug systems (e.g., when "record demo" is triggered)
- May be referenced in modding infrastructure for custom video capture

### Outgoing
- Directly uses Windows AVIFile API (AVIFileOpen, AVIStreamWrite, etc.)
- Depends on Windows GDI for bitmap handling (GlobalAllocPtr, BITMAPINFOHEADER)
- Uses C runtime for file operations (_access) and string formatting (sprintf)

## Design Patterns
- **Resource Acquisition Is Initialization (RAII)**: Constructor/destructor manage AVI resource lifecycle
- **Strategy Pattern**: `Grab()` delegates to `GrabAVI()` or `GrabRawFrame()` based on mode
- **Not inferable**: No clear use of other patterns (e.g., no visible factories or observers)
