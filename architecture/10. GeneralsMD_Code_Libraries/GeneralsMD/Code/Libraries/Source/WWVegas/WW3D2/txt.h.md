# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/txt.h

## Purpose
Header file defining the `TextTextureClass` for rendering text as textures in the SAGE engine.

## Responsibilities
- Manages text-to-texture conversion
- Caches texture parameters to avoid unnecessary rebuilds
- Provides access to generated textures and their metadata

## Key Types
- **TextTextureClass (Class)**: Manages text rendering into textures.
- **FontClass (Class)**: Forward declaration for font handling.
- **ConvertClass (Class)**: Forward declaration for texture conversion.
- **TextureClass (Class)**: Forward declaration for texture objects.

## Key Functions
### `Build_Texture`
- Purpose: Rebuilds the texture with new parameters.
- Calls: `Is_Texture_Valid` (indirectly via conditional logic).

### `Get_Texture`
- Purpose: Returns the generated texture pointer.
- Calls: None.

### `Get_Texture_Size`
- Purpose: Returns the size of the generated texture.
- Calls: None.

### `Is_Texture_Valid`
- Purpose: Checks if the texture needs rebuilding based on parameters.
- Calls: None.

## Globals
- None.

## Dependencies
- Forward declarations: `FontClass`, `ConvertClass`, `TextureClass`.
- Likely depends on texture/rendering systems (not shown in header).
