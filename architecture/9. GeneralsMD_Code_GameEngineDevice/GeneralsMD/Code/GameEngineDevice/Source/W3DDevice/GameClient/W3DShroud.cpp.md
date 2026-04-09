# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DShroud.cpp

## Purpose
Manages the rendering of fog-of-war/shroud effects for terrain and units in the game world.

## Responsibilities
- Initializes and manages shroud textures for the map
- Updates shroud visibility based on player knowledge
- Renders shroud effects using Direct3D textures
- Handles device reset recovery for shroud resources
- Supports fog interpolation for smooth transitions

## Key Types
- **W3DShroud (Class)**: Main shroud management class
- **W3DShroudLevel (Type)**: Represents shroud opacity level (0-255)
- **W3DShroudMaterialPassClass (Class)**: Material pass for shroud rendering
- **W3DMaskMaterialPassClass (Class)**: Material pass for mask rendering

## Key Functions
### init
- Purpose: Initializes shroud system for a new map
- Calls: DX8Wrapper::_Create_DX8_Surface, TextureLoader::Validate_Texture_Size

### render
- Purpose: Updates video memory with current shroud visibility
- Calls: DX8Wrapper::_Copy_DX8_Rects, fillBorderShroudData, interpolateFogLevels

### setShroudLevel
- Purpose: Sets the shroud level for a specific map cell
- Calls: None directly (modifies texture data)

### interpolateFogLevels
- Purpose: Smoothly interpolates between current and final fog states
- Calls: setShroudLevel

## Globals
- **DummyTexture (TextureClass*)**: Debug texture reference (not used in release)

## Dependencies
- Direct3D 8 via DX8Wrapper
- W3D rendering system (W3DShaderManager, TextureClass)
- Game world components (WorldHeightMap, PartitionManager)
- Global game data (TheGlobalData)
