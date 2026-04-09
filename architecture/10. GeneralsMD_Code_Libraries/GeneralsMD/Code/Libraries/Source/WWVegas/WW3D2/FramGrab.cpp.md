# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/FramGrab.cpp

## Purpose
Handles frame grabbing for video recording, supporting AVI and raw frame modes.

## Responsibilities
- Initializes AVI file creation and stream setup
- Manages frame conversion and storage
- Cleans up AVI resources on destruction
- Supports both AVI and raw frame output modes

## Key Types
- FrameGrabClass (Class): Main frame grabbing utility
- MODE (Enum): Recording mode (AVI or RAW)
- BITMAPINFOHEADER (Struct): Windows bitmap header for AVI stream

## Key Functions
### FrameGrabClass()
- Purpose: Constructor initializes frame grabbing with specified parameters
- Calls: AVIFileInit, AVIFileOpen, AVIFileCreateStream, AVIStreamSetFormat, GlobalAllocPtr

### ~FrameGrabClass()
- Purpose: Destructor cleans up AVI resources
- Calls: CleanupAVI

### CleanupAVI()
- Purpose: Releases AVI file and stream resources
- Calls: GlobalFreePtr, AVIStreamRelease, AVIFileRelease, AVIFileExit

### GrabAVI()
- Purpose: Writes frame data to AVI stream
- Calls: AVIStreamWrite

### ConvertFrame()
- Purpose: Converts frame data with vertical flip and color channel reordering
- Calls: None (direct memory manipulation)

## Globals
- None

## Dependencies
- vfw.h (AVIFile, AVIStream functions)
- windows.h (GlobalAllocPtr, BITMAPINFOHEADER)
- stdio.h, io.h (file operations)
- Not inferable: mmioFOURCC, OutputDebugString, SetRect
