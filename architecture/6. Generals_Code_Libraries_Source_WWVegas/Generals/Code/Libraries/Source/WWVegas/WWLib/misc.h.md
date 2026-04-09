# Generals/Code/Libraries/Source/WWVegas/WWLib/misc.h

## Purpose
Header file declaring video, system, and utility functions for the SAGE engine.

## Responsibilities
- Declares DirectDraw and video mode management functions
- Provides system utility functions (delay, vsync, processor detection)
- Defines palette and screen manipulation routines
- Exposes hardware capability queries
- Declares global video state variables

## Key Types
- None

## Key Functions
### Prep_Direct_Draw
- Purpose: Prepares DirectDraw subsystem
- Calls: Not inferable

### Set_Video_Mode
- Purpose: Sets video resolution and color depth
- Calls: Not inferable

### Set_Palette
- Purpose: Applies a palette to the display
- Calls: Not inferable

### Shake_Screen
- Purpose: Creates screen shake effect
- Calls: Not inferable

### Delay
- Purpose: Pauses execution for specified duration
- Calls: Not inferable

### Processor
- Purpose: Returns CPU type identifier
- Calls: Not inferable

### Operating_System
- Purpose: Returns OS type identifier
- Calls: Not inferable

## Globals
- CurrentPalette (unsigned char[768]): Current display palette
- Debug_Windowed (bool): Debug flag for windowed mode
- PaletteSurface (LPDIRECTDRAWSURFACE): DirectDraw surface for palette
- Audio_Focus_Loss_Function (void (*)(void)): Callback for audio focus loss
- SurfacesRestored (bool): Flag indicating surface restoration
- DirectDrawObject (LPDIRECTDRAW): DirectDraw object handle
- DirectDraw2Interface (LPDIRECTDRAW2): DirectDraw2 interface handle
- OperationgSystem (WORD): Detected operating system type
