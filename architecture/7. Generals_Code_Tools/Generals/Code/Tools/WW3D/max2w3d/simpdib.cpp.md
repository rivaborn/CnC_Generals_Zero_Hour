# Generals/Code/Tools/WW3D/max2w3d/simpdib.cpp

## Purpose
Manages a simple 8-bit device-independent bitmap (DIB) for graphics operations in the max2w3d tool.

## Responsibilities
- Creates and manages a DIB section with a palette
- Provides pixel manipulation methods
- Handles memory cleanup for DIB resources
- Supports both top-down and bottom-up DIB formats

## Key Types
- **SimpleDIBClass (Class)**: Wrapper for Windows DIB operations with palette support
- **PaletteClass (External)**: Used for color palette initialization (not defined here)

## Key Functions
### SimpleDIBClass::SimpleDIBClass
- Purpose: Constructs a DIB with specified dimensions and palette
- Calls: `new`, `CreateDIBSection`, `GetDC`, `ReleaseDC`

### SimpleDIBClass::~SimpleDIBClass
- Purpose: Cleans up DIB resources
- Calls: `delete[]`, `DeleteObject`

### SimpleDIBClass::Clear
- Purpose: Fills the DIB with a specified color
- Calls: `memset`

### SimpleDIBClass::Set_Pixel
- Purpose: Sets a pixel at given coordinates to a specified color
- Calls: None

## Globals
- None

## Dependencies
- Key includes: `simpdib.h`
- External symbols: `BITMAPINFO`, `RGBQUAD`, `HDC`, `HWND`, `CreateDIBSection`, `GetDC`, `ReleaseDC`, `DeleteObject`, `memset`
