# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/dib.h

## Purpose
Defines a class for managing 8-bit device-independent bitmaps (DIBs) with palette support.

## Responsibilities
- Create and manage 8-bit DIBs with associated palettes
- Provide access to DIB properties (handle, dimensions, surface)
- Support clearing the DIB with a specified color

## Key Types
- **DIB8Class (Class)**: Wrapper for 8-bit DIBs with palette support and surface access

## Key Functions
### DIB8Class()
- Purpose: Constructs a DIB8Class instance with specified dimensions and palette
- Calls: Not inferable

### ~DIB8Class()
- Purpose: Destroys the DIB8Class instance and releases resources
- Calls: Not inferable

### Get_Handle()
- Purpose: Returns the HBITMAP handle of the DIB
- Calls: None

### Get_Width()
- Purpose: Returns the width of the DIB in pixels
- Calls: None

### Get_Height()
- Purpose: Returns the height of the DIB in pixels
- Calls: None

### Get_Surface()
- Purpose: Returns a reference to the BSurface wrapping the pixel buffer
- Calls: None

### Clear()
- Purpose: Clears the DIB with a specified color value
- Calls: Not inferable

## Globals
- None

## Dependencies
- `always.h`, `bsurface.h`, `palette.h`, `win.h`
- `HBITMAP`, `BITMAPINFO`, `Surface`, `PaletteClass`, `HWND`
