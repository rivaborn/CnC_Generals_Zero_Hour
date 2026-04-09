# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/framgrab.h

## Purpose
Defines the `FrameGrabClass` for capturing game frames as raw images or AVI video.

## Responsibilities
- Capture frames in RAW or AVI format
- Manage AVI file creation and cleanup
- Convert frame data for AVI compatibility
- Provide access to captured frame data

## Key Types
- **FrameGrabClass (Class)**: Handles frame capture and AVI generation.
- **MODE (Enum)**: Specifies capture mode (RAW or AVI).
- **RAW (Enum)**: Raw frame capture mode.
- **AVI (Enum)**: AVI video capture mode.

## Key Functions
### FrameGrabClass(const char *filename, MODE mode, int width, int height, int bitdepth, float framerate)
- Purpose: Constructor initializes frame capture settings.
- Calls: None.

### ConvertGrab(void *BitmapPointer)
- Purpose: Converts and saves the captured frame.
- Calls: `GrabAVI` or `GrabRawFrame`.

### Grab(void *BitmapPointer)
- Purpose: Captures a frame from the given bitmap pointer.
- Calls: `ConvertGrab`.

### GrabAVI(void *BitmapPointer)
- Purpose: Captures a frame and writes it to an AVI file.
- Calls: `ConvertFrame`, `CleanupAVI`.

### GrabRawFrame(void *BitmapPointer)
- Purpose: Saves a raw frame to disk.
- Calls: None.

### CleanupAVI()
- Purpose: Releases AVI resources.
- Calls: None.

### ConvertFrame(void *BitmapPointer)
- Purpose: Converts frame data to AVI-compatible format.
- Calls: None.

## Globals
- **Filename (const char *)**: Output file path.
- **FrameRate (
