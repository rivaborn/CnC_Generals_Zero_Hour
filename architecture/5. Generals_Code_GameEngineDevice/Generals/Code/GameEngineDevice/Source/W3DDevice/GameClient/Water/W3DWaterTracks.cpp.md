# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Water/W3DWaterTracks.cpp

## Purpose
Manages water wave effects and splash marks on the water surface in the SAGE engine.

## Responsibilities
- Render animated water waves with dynamic UV coordinates, scaling, scrolling, and alpha
- Manage wave lifecycle (creation, movement, fading)
- Support wave editing in-game (F5-F8 hotkeys)
- Load/save wave tracks from/to .wak files
- Handle multiple wave types (pond, ocean, radial, stationary)

## Key Types
- **waveType (Enum)**: Enumerates different wave types (Pond, Ocean, CloseOcean, etc.)
- **waveInfo (Struct)**: Contains wave parameters (width, height, velocity, fade time)
- **WaterTracksObj (Class)**: Represents a single wave track with rendering logic
- **WaterTracksRenderSystem (Class)**: Manages collection of wave tracks

## Key Functions
### WaterTracksObj::render
- Purpose: Renders a wave track with current state
- Calls: DX8Wrapper::Set_Texture, DX8Wrapper::Set_Vertex_Buffer

### WaterTracksRenderSystem::render
- Purpose: Renders all active wave tracks
- Calls: DX8Wrapper::Set_Material, DX8Wrapper::Set_Shader, WaterTracksObj::render

### WaterTracksRenderSystem::loadTracks
- Purpose: Loads wave tracks from .wak file
- Calls: TheFileSystem->openFile, WaterTracksObj::init

### TestWaterUpdate
- Purpose: Handles in-game wave editing via hotkeys (F5-F8)
- Calls: TheWaterTracksRenderSystem->bindTrack, TheTacticalView->screenToTerrain

## Globals
- **TheWaterTracksRenderSystem (WaterTracksRenderSystem*)**: Singleton for track drawing system
- **pauseWaves (Bool)**: Flag to pause wave animations during editing
- **waveTypeInfo (waveInfo[WaveTypeMax])**: Array of wave type configurations
- **ApplicationHWnd (HWND)**: Handle to application window for mouse input

## Dependencies
- W3DDevice/GameClient/W3DWaterTracks.h
- GameClient/InGameUI.h
- GameLogic/TerrainLogic.h
- Common/GlobalData.h
- WW3D2/DX8Wrapper.h
- DirectX 8 vertex buffer and render state APIs
