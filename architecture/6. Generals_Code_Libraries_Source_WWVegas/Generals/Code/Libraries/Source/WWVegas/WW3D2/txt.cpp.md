# Generals/Code/Libraries/Source/WWVegas/WW3D2/txt.cpp

## Purpose
Manages text rendering as textures in the SAGE engine, handling texture creation and validation for font-based UI elements.

## Responsibilities
- Creates and manages text textures for rendering
- Validates existing textures to avoid unnecessary rebuilds
- Handles texture sizing and formatting for hardware compatibility
- Manages font rendering into texture surfaces

## Key Types
- **TextTextureClass (Class)**: Main class handling text texture creation and management
- **ConvertClass (Pointer)**: Reference to color conversion utility (external)
- **FontClass (Pointer)**: Reference to font rendering system (external)

## Key Functions
### `Is_Texture_Valid`
- Purpose: Checks if existing texture matches current rendering parameters
- Calls: None

### `Build_Texture`
- Purpose: Creates or updates a text texture based on input parameters
- Calls: `Is_Texture_Valid`, `nstrdup`, `String_Pixel_Width`, `Get_Height`, `Print`, `Find_POT`, `Fill`, `Blit_From`

## Globals
- **default_font_palette (array)**: Static palette for font rendering (16 bytes)

## Dependencies
- Key includes: `<stdio.h>`, `<math.h>`, "pot.h", "txt.h", "bsurface.h", "texture.h", "font.h", "nstrdup.h"
- External symbols: `Find_POT`, `REF_PTR_RELEASE`, `nstrdup`, `FontClass` methods, `ConvertClass` methods
