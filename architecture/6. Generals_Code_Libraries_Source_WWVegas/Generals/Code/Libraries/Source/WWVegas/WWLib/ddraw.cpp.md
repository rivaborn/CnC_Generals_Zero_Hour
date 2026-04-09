# Generals/Code/Libraries/Source/WWVegas/WWLib/ddraw.cpp

## Purpose
Handles DirectDraw initialization, video mode management, and palette operations for the game.

## Responsibilities
- Manages DirectDraw object lifecycle (creation, mode setting, cleanup)
- Handles palette fading and setting
- Processes DirectDraw errors with user feedback
- Queries video hardware capabilities
- Synchronizes with vertical blank and blit operations

## Key Types
- `DirectDrawObject` (LPDIRECTDRAW): Main DirectDraw interface pointer
- `DirectDraw2Interface` (LPDIRECTDRAW2): DirectDraw 2 interface pointer
- `PaletteEntries` (PALETTEENTRY[256]): Stores palette data
- `CurrentPalette` (unsigned char[768]): Current active palette

## Key Functions
### `Set_Palette`
- Purpose: Fades between palettes over time with optional callback
- Calls: `Set_Palette` (internal), `callback()`

### `Process_DD_Result`
- Purpose: Displays error messages for DirectDraw failures
- Calls: `MessageBox`, `DirectDrawErrorHandler`

### `Set_Video_Mode`
- Purpose: Initializes DirectDraw and sets display resolution
- Calls: `Prep_Direct_Draw`, `DirectDrawObject->SetDisplayMode`, `DirectDrawObject->CreatePalette`

### `Wait_Vert_Blank`
- Purpose: Synchronizes with vertical blank interval
- Calls: `DirectDrawObject->WaitForVerticalBlank`

### `Wait_Blit`
- Purpose: Waits for blit operations to complete
- Calls: `PaletteSurface->GetBltStatus`

## Globals
- `DirectDrawObject` (LPDIRECTDRAW): Main DirectDraw interface
- `DirectDraw2Interface` (LPDIRECTDRAW2): DirectDraw 2 interface
- `CurrentPalette` (unsigned char[768]): Currently active palette
- `Debug_Windowed` (bool): Windowed mode debug flag
- `DirectDrawErrorHandler` (function pointer): Custom error handler

## Dependencies
- DirectDraw COM interfaces (`LPDIRECTDRAW`, `LPDIRECTDRAW2`)
- `PaletteClass` from game codebase
- `CDTimerClass` for timing palette fades
- Windows API (`MessageBox`, `HWND`)
- DirectDraw constants and structures (`DDCAPS`, `DDPCAPS`, etc.)
