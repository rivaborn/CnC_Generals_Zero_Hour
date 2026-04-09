# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/dib.cpp

## Purpose
Implements a device-independent bitmap (DIB) class for 8-bit color rendering in the SAGE engine.

## Responsibilities
- Manages creation/destruction of DIB sections
- Handles palette initialization for 8-bit color
- Provides pixel access and clearing functionality
- Wraps DIB in a BSurface for rendering operations

## Key Types
- DIB8Class (Class): 8-bit DIB wrapper with palette support
- BITMAPINFO (Struct): Windows bitmap header structure
- BSurface (Class): Internal surface wrapper (not defined here)

## Key Functions
### DIB8Class::DIB8Class
- Purpose: Constructs an 8-bit DIB with specified dimensions and palette
- Calls: GetDC, CreateDIBSection, ReleaseDC, new (BSurface)

### DIB8Class::~DIB8Class
- Purpose: Destroys DIB resources and cleanup
- Calls: delete (for Info, Surface), DeleteObject (Handle)

### DIB8Class::Clear
- Purpose: Fills the DIB with a specified color value
- Calls: memset

## Globals
None

## Dependencies
- Key includes: always.h, dib.h, <math.h>
- External symbols: BITMAPINFO, BITMAPINFOHEADER, RGBQUAD, HWND, HDC, CreateDIBSection, DeleteObject, GetDC, ReleaseDC, memset
