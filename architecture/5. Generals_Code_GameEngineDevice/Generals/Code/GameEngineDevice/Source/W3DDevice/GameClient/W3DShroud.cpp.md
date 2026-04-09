# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DShroud.cpp

## Purpose
Manages the rendering of fog-of-war/shroud effects for terrain and units in the game world.

## Responsibilities
- Initializes and manages shroud textures for the map
- Updates shroud visibility based on player knowledge
- Handles Direct3D device resets and resource reacquisition
- Provides methods to query/set shroud levels per cell
- Renders shroud overlay during scene rendering

## Key Types
- **W3DShroud (Class)**: Main shroud management class
- **W3DShroudLevel (Type)**: Represents shroud opacity (0-255)
- **W3DShroudMaterialPassClass (Class)**: Material pass for shroud rendering
- **W3DMaskMaterialPassClass (Class)**: Material pass for mask rendering

## Key Functions
### `init`
- Purpose: Initializes shroud system for a new map
- Calls: `ReleaseResources`, `ReAcquireResources`, `fillShroudData`

### `render`
- Purpose: Updates video memory with visible shroud data
- Calls: `fillBorderShroudData`, `interpolateFogLevels`, `DX8Wrapper::_Copy_DX8_Rects`

### `setShroudLevel`
- Purpose: Sets shroud level for a specific cell
- Calls: None directly (modifies texture data)

### `interpolateFogLevels`
- Purpose: Animates fog-of-war changes over time
- Calls: `setShroudLevel`

## Globals
- **DummyTexture (TextureClass*)**: Debug texture reference (unused in release)

## Dependencies
- Direct3D 8 via `DX8Wrapper`
- `TextureClass` for texture management
- `WorldHeightMap` for terrain data
- `W3DShaderManager` for shader states
- `PartitionManager` for shroud updates
