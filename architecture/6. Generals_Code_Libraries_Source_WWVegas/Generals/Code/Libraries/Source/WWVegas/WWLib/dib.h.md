# Generals/Code/Libraries/Source/WWVegas/WWLib/dib.h

## Purpose
Defines a class for managing 8-bit device-independent bitmaps (DIBs) with palette support.

## Responsibilities
- Create and manage 8-bit DIBs
- Provide access to DIB properties (handle, dimensions, surface)
- Clear the DIB with a specified color
- Wrap a BSurface around the pixel buffer

## Key Types
- DIB8Class (Class): Manages 8-bit DIBs with palette support

## Key Functions
### DIB8Class::DIB8Class
- Purpose: Constructs a DIB8Class instance
- Calls: Not inferable

### DIB8Class::~DIB8Class
- Purpose: Destroys the DIB8Class instance
- Calls: Not inferable

### DIB8Class::Get_Handle
- Purpose: Returns the HBITMAP handle
- Calls: None

### DIB8Class::Get_Width
- Purpose: Returns the DIB width
- Calls: None

### DIB8Class::Get_Height
- Purpose: Returns the DIB height
- Calls: None

### DIB8Class::Get_Surface
- Purpose: Returns a reference to the wrapped BSurface
- Calls: None

### DIB8Class::Clear
- Purpose: Clears the DIB with a specified color
- Calls: Not inferable

## Globals
- None

## Dependencies
- always.h
- bsurface.h
- palette.h
- win.h
