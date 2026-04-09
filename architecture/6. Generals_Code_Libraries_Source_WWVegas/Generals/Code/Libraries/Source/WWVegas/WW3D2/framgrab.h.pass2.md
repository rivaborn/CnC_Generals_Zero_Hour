# Generals/Code/Libraries/Source/WWVegas/WW3D2/framgrab.h - Enhanced Analysis

## Architectural Role
This file defines the `FrameGrabClass`, a utility for capturing game frames as raw images or AVI video. It integrates with the rendering pipeline to export frames, likely used for debugging, modding, or cinematic creation.

## Cross-References
### Incoming
- Rendering subsystem (calls `Grab()` to capture frames)
- Debug tools (likely invoke `FrameGrabClass` for screenshots)
- Modding tools (use raw/AVI export for content creation)

### Outgoing
- Windows API (`vfw.h` for AVI handling)
- File I/O (for raw frame saving)
- Memory management (for bitmap buffers)

## Design Patterns
- **Facade Pattern**: Encapsulates AVI/VFW complexity behind a simple interface.
- **Strategy Pattern**: `Grab()` delegates to `GrabAVI()` or `GrabRawFrame()` based on mode.
- **Resource Management**: `CleanupAVI()` handles AVI resource deallocation.
