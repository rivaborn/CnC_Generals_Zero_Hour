# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Water/W3DWaterTracks.cpp

## Purpose
Manages water wave effects and splash marks on the water surface in the SAGE engine.

## Responsibilities
- Render animated water waves with dynamic UV coordinates, scaling, scrolling, and alpha
- Manage wave lifecycle (creation, movement, fading)
- Support wave editing tools for map creation
- Handle wave type configurations and parameters
- Integrate with the terrain system and rendering pipeline

## Key Types
- **waveType (Enum)**: Different wave types (Pond, Ocean, etc.)
- **waveInfo (Struct)**: Configuration data for each wave type
- **WaterTracksObj (Class)**: Individual wave track object with rendering and animation logic
- **WaterTracksRenderSystem (Class)**: Manages collection of wave tracks and rendering system

## Key Functions
### WaterTracksObj::render
- Purpose: Renders the wave object with current animation state
- Calls: DX8Wrapper::Set_Texture, DX8Wrapper::Set_DX8_Render_State

### WaterTracksRenderSystem::render
- Purpose: Renders all active wave tracks
- Calls: WaterTracksObj::render, DX8Wrapper::Set_DX8_Render_State

### TestWaterUpdate
- Purpose: Handles wave editing functionality in-game
- Calls: TheWaterTracksRenderSystem methods, TheInGameUI->message

## Globals
- **TheWaterTracksRenderSystem (WaterTracksRenderSystem*)**: Singleton for track drawing system
- **pauseWaves (Bool)**: Flag to pause wave animations
- **waveTypeInfo (waveInfo[WaveTypeMax])**: Configuration data for each wave type
- **ApplicationHWnd (HWND)**: Handle to application window

## Dependencies
- W3DDevice/GameClient headers (W3DWaterTracks.h, W3DShaderManager.h, etc.)
- GameClient headers (InGameUI.h, Water.h)
- GameLogic headers (TerrainLogic.h)
- Common headers (GlobalData.h, UnicodeString.h)
- WW3D2/DX8Wrapper.h for DirectX rendering
- DirectX 8 headers for rendering states
