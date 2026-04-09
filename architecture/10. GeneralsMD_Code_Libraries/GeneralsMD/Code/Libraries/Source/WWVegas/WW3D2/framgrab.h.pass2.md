# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/framgrab.h - Enhanced Analysis

## Architectural Role
This file defines the `FrameGrabClass`, which is part of the SAGE engine's rendering subsystem. It provides functionality for capturing game frames, either as raw images or AVI videos, which is likely used for debugging, replay systems, or modding tools.

## Cross-References
### Incoming
- Not inferable from header alone.

### Outgoing
- Uses Windows API (`windows.h`, `windowsx.h`, `vfw.h`) for AVI file handling.
- Likely called by rendering or debugging subsystems (e.g., `W3D` or `Debug` modules).

## Design Patterns
- **Strategy Pattern**: The `MODE` enum and conditional logic in `ConvertGrab` suggest different capture strategies (RAW/AVI) can be selected at runtime.
- **Resource Management**: `CleanupAVI` indicates RAII-like handling for AVI resources, though not fully implemented in the header.
- **Facade Pattern**: Abstracts AVI/VFW complexity behind a simple interface for frame capture.
