# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/ddraw.cpp

## Purpose
Handles DirectDraw initialization, video mode management, and palette operations for the game.

## Responsibilities
- Manages DirectDraw object lifecycle (creation, mode setting, cleanup)
- Handles palette operations (loading, fading, synchronization)
- Provides video hardware capability queries
- Processes DirectDraw errors with user feedback
- Synchronizes with vertical blank intervals

## Key Types
- `DirectDrawObject` (LPDIRECTDRAW): Main DirectDraw interface pointer
- `PaletteEntries` (PALETTEENTRY[256]): Stores current palette data
- `CurrentPalette` (unsigned char[768]): Tracks active palette in RGB format
- `DDCAPS` (struct): DirectDraw capabilities structure (external)

## Key Functions
### `Set_Palette`
- Purpose: Fades between palettes over time with optional callback
- Calls: `Set_Palette` (internal), `callback` (user-provided)

### `Process_DD_Result`
- Purpose: Handles DirectDraw error codes with debug messages
- Calls: `MessageBox`, `DirectDrawErrorHandler` (if set)

### `Set_Video_Mode`
- Purpose: Initializes DirectDraw and sets display resolution
- Calls: `Prep_Direct_Draw`, `DirectDrawObject->SetDisplayMode`, `CreatePalette`

### `Wait_Vert_Blank`
- Purpose: Synchronizes with vertical blank interval
- Calls: `DirectDrawObject->WaitForVerticalBlank`

### `Get_Video_Hardware_Capabilities`
- Purpose: Queries DirectDraw hardware feature support
- Calls: `DirectDrawObject->GetCaps`

## Globals
- `DirectDrawObject` (LPDIRECTDRAW): Main DirectDraw interface
- `PalettePtr` (LPDIRECTDRAWPALETTE): Current palette object
- `CurrentPalette` (unsigned char[768]): Active palette storage
- `CanVblankSync` (bool): Tracks vertical blank sync availability
- `DirectDrawErrorHandler` (function pointer): Custom error handler

## Dependencies
- DirectDraw COM interfaces (`LPDIRECTDRAW`, `LPDIRECTDRAW2`)
- Windows API (`MessageBox`, `HWND`)
- Game-specific types (`PaletteClass`, `MainWindow`)
- DirectDraw constants (`DDERR_*`, `DDCAPS_*`)
