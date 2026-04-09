# Generals/Code/Libraries/Source/WWVegas/WW3D2/txt.h

## Purpose
Header file defining the `TextTextureClass` for rendering text as textures in the SAGE engine.

## Responsibilities
- Manages text-to-texture conversion
- Caches texture parameters to avoid unnecessary rebuilds
- Provides access to generated textures and their metadata

## Key Types
- `FontClass` (Class): Font rendering interface
- `ConvertClass` (Class): Texture conversion interface
- `TextureClass` (Class): Renderable texture object
- `TextTextureClass` (Class): Text-to-texture conversion and caching

## Key Functions
### `TextTextureClass::Build_Texture`
- Purpose: Rebuilds the texture with new parameters
- Calls: `Is_Texture_Valid`

### `TextTextureClass::Get_Texture`
- Purpose: Returns the generated texture pointer
- Calls: None

### `TextTextureClass::Get_Texture_Size`
- Purpose: Returns the size of the generated texture
- Calls: None

### `TextTextureClass::Is_Texture_Valid`
- Purpose: Checks if the texture needs rebuilding
- Calls: None

## Globals
- None

## Dependencies
- Forward declarations: `FontClass`, `ConvertClass`, `TextureClass`
- External symbols: None defined here
