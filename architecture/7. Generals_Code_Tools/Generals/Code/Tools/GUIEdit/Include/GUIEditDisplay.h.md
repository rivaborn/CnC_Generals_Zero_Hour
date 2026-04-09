# Generals/Code/Tools/GUIEdit/Include/GUIEditDisplay.h

## Purpose
Defines a stripped-down display class for the GUI edit tool, inheriting from Display.

## Responsibilities
- Provides basic 2D drawing primitives (lines, rectangles, images)
- Manages clipping regions
- Stubs out advanced display features (video buffers, shroud, lighting)
- Supports performance metrics (FPS, draw calls)

## Key Types
- **GUIEditDisplay (Class)**: Lightweight display implementation for GUI editor
- **VideoBuffer (Class)**: Forward-declared video buffer type

## Key Functions
### drawLine
- Purpose: Draw a line with specified color and width
- Calls: None

### drawOpenRect
- Purpose: Draw a rectangular border with specified color and width
- Calls: None

### drawFillRect
- Purpose: Draw a filled rectangle with specified color
- Calls: None

### drawImage
- Purpose: Draw an image within screen coordinates with optional color and mode
- Calls: None

### setClipRegion
- Purpose: Set the clipping region for subsequent draws
- Calls: None

### enableClipping
- Purpose: Enable/disable clipping
- Calls: None

### createVideoBuffer
- Purpose: Stub for video buffer creation (returns NULL)
- Calls: None

### getAverageFPS
- Purpose: Stub for FPS calculation (returns 0)
- Calls: None

## Globals
- None

## Dependencies
- `Display` (base class)
- `Image`, `IRegion2D`, `Color`, `DrawImageMode` (types)
- `VideoBuffer` (forward reference)
