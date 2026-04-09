# Generals/Code/Tools/Launcher/loadbmp.h

## Purpose
Header file defining the LoadBmp class for loading and displaying bitmap images in a Windows window.

## Responsibilities
- Load bitmap files from disk
- Create and manage Windows bitmap and palette handles
- Render bitmaps in a specified window
- Handle initialization and cleanup of bitmap resources

## Key Types
- LoadBmp (Class): Manages loading and displaying of bitmap images in a Windows window

## Key Functions
### LoadBmp()
- Purpose: Default constructor for LoadBmp class
- Calls: None

### ~LoadBmp()
- Purpose: Destructor for LoadBmp class
- Calls: None

### init()
- Purpose: Initializes the bitmap from a file and associates it with a window
- Calls: None

### drawBmp()
- Purpose: Renders the loaded bitmap in the associated window
- Calls: None

## Globals
- None

## Dependencies
- stdlib.h
- stdio.h
- wstypes.h
- winblows.h
- HBITMAP (Windows GDI)
- HPALETTE (Windows GDI)
- HWND (Windows handle)
- bit8 (custom type from wstypes.h)
