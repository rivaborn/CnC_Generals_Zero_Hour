# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/misc.h

## Purpose
Header file declaring video, system, and utility functions for the SAGE engine.

## Responsibilities
- Declares DirectDraw and video mode management functions
- Provides system utility functions (delay, vsync, processor detection)
- Defines palette and surface manipulation routines
- Declares hardware capability detection functions
- Contains screen shake and rectangle clipping utilities

## Key Types
- None (header-only file)

## Key Functions
### Prep_Direct_Draw
- Purpose: Prepares DirectDraw subsystem
- Calls: Not inferable

### Set_Video_Mode
- Purpose: Sets video display mode
- Calls: Not inferable

### Set_Palette
- Purpose: Applies color palette to display
- Calls: Not inferable

### Shake_Screen
- Purpose: Creates screen shake effect
- Calls: Not inferable

### Delay
- Purpose: Pauses execution for specified duration
- Calls: Not inferable

### Processor
- Purpose: Detects CPU type
- Calls: Not inferable

## Globals
- CurrentPalette (unsigned char[768]): Current display palette
- Debug_Windowed (bool): Windowed mode debug flag
- PaletteSurface (LPDIRECTDRAWSURFACE): DirectDraw surface for palette
- Audio_Focus_Loss_Function (void (*)(void)): Callback for audio focus loss
- SurfacesRestored (bool): Flag indicating surface restoration
- DirectDrawObject (LPDIRECTDRAW): DirectDraw object interface
- DirectDraw2Interface (LPDIRECTDRAW2): DirectDraw2 interface
- OperationgSystem (WORD): Detected operating system

## Dependencies
- win.h, ddraw.h: Windows and DirectDraw headers
