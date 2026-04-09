# Generals/Code/Libraries/Source/WWVegas/WW3D2/framgrab.h

## Purpose
Defines the `FrameGrabClass` for capturing game frames as raw images or AVI video.

## Responsibilities
- Initialize frame capture (raw or AVI)
- Capture and convert frames
- Manage AVI file handling and cleanup
- Provide access to captured frame data

## Key Types
- **FrameGrabClass (Class)**: Manages frame capture functionality.
- **MODE (Enum)**: Capture mode (RAW or AVI).
- **RAW (Enum)**: Raw frame capture mode.
- **AVI (Enum)**: AVI video capture mode.

## Key Functions
### FrameGrabClass()
- Purpose: Constructor for frame capture initialization.
- Calls: Not inferable.

### ~FrameGrabClass()
- Purpose: Destructor for cleanup.
- Calls: Not inferable.

### ConvertGrab()
- Purpose: Converts captured frame data.
- Calls: `ConvertFrame()`.

### Grab()
- Purpose: Captures a frame based on the selected mode.
- Calls: `GrabAVI()` or `GrabRawFrame()`.

### GrabAVI()
- Purpose: Captures a frame and writes it to an AVI file.
- Calls: `ConvertFrame()`, `CleanupAVI()`.

### GrabRawFrame()
- Purpose: Saves a raw frame to disk.
- Calls: Not inferable.

### CleanupAVI()
- Purpose: Cleans up AVI resources.
- Calls: Not inferable.

### ConvertFrame()
- Purpose: Converts frame data to AVI-compatible format.
- Calls: Not inferable.

## Globals
None.

## Dependencies
- `always.h`, `windows.h`, `windowsx.h`, `vfw.h`
- `PAVIFILE`, `PAVISTREAM`, `
