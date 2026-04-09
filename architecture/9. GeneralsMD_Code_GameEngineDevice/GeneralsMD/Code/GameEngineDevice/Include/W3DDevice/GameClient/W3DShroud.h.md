# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DShroud.h

## Purpose
Defines classes for handling fog-of-war (shroud) rendering in the W3D engine.

## Responsibilities
- Manages shroud texture projection and rendering
- Handles material passes for shroud and mask effects
- Provides interface for setting/getting shroud levels
- Supports resource management during device resets

## Key Types
- **W3DShroudMaterialPassClass (Class)**: Custom material pass for shroud texture projection
- **W3DMaskMaterialPassClass (Class)**: Generic texture projection material pass
- **W3DShroud (Class)**: Main shroud rendering system
- **W3DShroudLevel (typedef)**: Shroud intensity level (UnsignedByte)

## Key Functions
### W3DShroud::render
- Purpose: Renders the current shroud state from a given camera
- Calls: Not inferable

### W3DShroud::init
- Purpose: Initializes the shroud system with map data
- Calls: Not inferable

### W3DShroud::fillShroudData
- Purpose: Sets all shroud cells to a constant value
- Calls: Not inferable

### W3DShroud::setShroudLevel
- Purpose: Updates the shroud level at a specific cell
- Calls: Not inferable

## Globals
- None

## Dependencies
- `WW3D2/matpass.h` (MaterialPassClass)
- `WW3D2/dx8wrapper.h` (DirectX 8 wrapper)
- `TextureClass`, `SurfaceClass` (external texture/surface classes)
- `CameraClass`, `WorldHeightMap` (external game classes)
