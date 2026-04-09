# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DDisplay.cpp

## Purpose
Handles the 3D display rendering and management for the W3D game engine, including performance monitoring, asset management, and screen capture functionality.

## Responsibilities
- Manages 3D/2D rendering scenes and asset loading
- Provides performance statistics and debugging tools
- Handles screen captures and video recording
- Manages dynamic lighting and terrain rendering
- Implements asset preloading and purging mechanisms

## Key Types
- `W3DDisplay` (Class): Main display manager for 3D rendering
- `StatDumpClass` (Class): Handles performance statistics dumping
- `RTS3DScene`/`RTS2DScene`/`RTS3DInterfaceScene` (Pointers): Scene management objects

## Key Functions
### `drawFramerateBar`
- Purpose: Renders a visual framerate indicator bar
- Calls: `TheDisplay->drawFillRect`, `timeGetTime`

### `getPerformanceCounter`
- Purpose: Retrieves high-resolution performance counter value
- Calls: `QueryPerformanceCounter`

### `Reset_D3D_Device`
- Purpose: Resets the Direct3D device state
- Calls: `DX8Wrapper` functions, scene recreation methods

### `takeScreenShot`
- Purpose: Captures and saves the current screen as BMP/TGA
- Calls: `CreateFile`, `WriteFile`, `DX8Wrapper::_Get_DX8_Front_Buffer`

### `dumpModelAssets`
- Purpose: Dumps used model/texture assets to file (debug only)
- Calls: `fopen`, `fprintf`, scene iteration methods

## Globals
- `START_CUMU_FRAME` (Int): Frame counter for performance tracking
- `TheStatDump` (StatDumpClass): Global statistics dumper instance

## Dependencies
- Direct3D 8 (DX8Wrapper)
- WW3D2 rendering library
- Game engine core systems (GameLogic, GameClient)
- File system and asset management utilities
- Performance timing utilities (PerfTimer)
