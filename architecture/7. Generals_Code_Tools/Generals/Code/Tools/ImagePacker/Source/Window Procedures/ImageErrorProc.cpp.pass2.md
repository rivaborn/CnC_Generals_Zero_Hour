# Generals/Code/Tools/ImagePacker/Source/Window Procedures/ImageErrorProc.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI layer for error reporting in the ImagePacker tool, bridging the core image processing logic (ImagePacker class) with Windows dialog procedures. It serves as a user-facing error handler for the tool's build pipeline.

## Cross-References
### Incoming
- Likely called from the main ImagePacker tool when image processing errors occur (via `DialogBox` or similar)

### Outgoing
- Calls into `TheImagePacker` (ImagePacker class) for image data
- Uses Windows API (`SendMessage`, `EndDialog`) for dialog management
- References resources defined in "Resource.h" (dialog controls)

## Design Patterns
- **Dialog Controller**: Manages the error dialog's behavior and state
- **Status Flag Checking**: Uses bit flags (via `BitTest`) to determine error types (TOOBIG, INVALIDCOLORDEPTH)
- **Global Singleton Access**: Relies on `TheImagePacker` global for tool state (not ideal for modularity)
