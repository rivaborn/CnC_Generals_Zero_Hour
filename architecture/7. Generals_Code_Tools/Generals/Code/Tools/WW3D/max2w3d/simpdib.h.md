# Generals/Code/Tools/WW3D/max2w3d/simpdib.h

## Purpose
Defines a simple DIB (Device-Independent Bitmap) wrapper class for bitmap manipulation in the max2w3d tool.

## Responsibilities
- Manages bitmap creation, pixel access, and memory handling
- Provides basic bitmap operations (clear, set pixel)
- Handles palette association for the bitmap
- Tracks bitmap dimensions and memory layout

## Key Types
- **SimpleDIBClass (Class)**: Wrapper for bitmap operations with palette support

## Key Functions
### SimpleDIBClass/SimpleDIBClass
- Purpose: Constructor that creates a DIB with specified dimensions and palette
- Calls: Not inferable (constructor implementation not shown)

### SimpleDIBClass/Clear
- Purpose: Clears the bitmap with a specified color
- Calls: Not inferable

### SimpleDIBClass/Set_Pixel
- Purpose: Sets a pixel at specified coordinates to a given color
- Calls: Not inferable

## Globals
- None

## Dependencies
- `always.h`, `Max.h`, `win.h`, `palette.h`
- `HWND`, `HBITMAP`, `BITMAPINFO`, `PaletteClass`
