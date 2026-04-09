# Generals/Code/Libraries/Source/WWVegas/WW3D2/FramGrab.cpp

## Purpose
Implements frame capture functionality for AVI video recording in the SAGE engine.

## Responsibilities
- Manages AVI file creation and stream handling
- Converts and stores frame data in AVI format
- Supports raw frame capture (unimplemented)
- Handles bitmap format conversion for video recording

## Key Types
- FrameGrabClass (Class): Main frame capture handler
- MODE (Enum): Capture mode (AVI/RAW)
- BITMAPINFOHEADER (Struct): Windows bitmap header for AVI stream

## Key Functions
### FrameGrabClass()
- Purpose: Initializes AVI file and stream for recording
- Calls: AVIFileInit, AVIFileOpen, AVIFileCreateStream, AVIStreamSetFormat, GlobalAllocPtr

### ~FrameGrabClass()
- Purpose: Cleans up AVI resources on destruction
- Calls: CleanupAVI

### CleanupAVI()
- Purpose: Releases AVI file and stream resources
- Calls: GlobalFreePtr, AVIStreamRelease, AVIFileRelease, AVIFileExit

### GrabAVI()
- Purpose: Writes frame data to AVI stream
- Calls: AVIStreamWrite

### ConvertFrame()
- Purpose: Converts bitmap format (flip + byte reordering)
- Calls: None

## Globals
- None

## Dependencies
- AVIFile API (AVIFileInit, AVIFileOpen, etc.)
- Windows GDI (BITMAPINFOHEADER, GlobalAllocPtr)
- C runtime (sprintf, _access)
