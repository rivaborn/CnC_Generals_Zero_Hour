# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/render2dsentence.cpp

## Purpose
Handles 2D text rendering in the SAGE engine, managing fonts, text layout, and rendering operations.

## Responsibilities
- Manages font characters and their rendering data
- Handles text layout, wrapping, and positioning
- Builds and renders text as textures
- Supports clipping and additive blending modes
- Maintains surface and texture resources

## Key Types
- **Render2DSentenceClass**: Main class for 2D text rendering
- **FontCharsClass**: Font character data management
- **FontCharsClassCharDataStruct**: Per-character rendering data
- **FontCharsBuffer**: Buffer for character pixel data

## Key Functions
### FindStartingXPos
- Purpose: Calculates starting X position for text rendering
- Calls: Not inferable (truncated)

### Build_Sentence_Not_Centered
- Purpose: Builds text layout without centering
- Calls: Not inferable (truncated)

### Get_Text_Extents
- Purpose: Calculates text dimensions
- Calls: Font->Get_Char_Height(), Font->Get_Char_Spacing()

### Build_Textures
- Purpose: Converts pending surfaces to textures
- Calls: W3DNEW TextureClass, DX8Wrapper::_Copy_DX8_Rects

### Create_GDI_Font
- Purpose: Creates GDI font for character rendering
- Calls: ::CreateFont, ::CreateDIBSection, ::CreateCompatibleDC

## Globals
- **no_TEST_PLACEMENT**: Debug flag for text alignment markers
- **TEXTURE_OFFSET**: Texture offset constant

## Dependencies
- render2dsentence.h, surfaceclass.h, texture.h, wwprofile.h, wwmemlog.h, dx8wrapper.h
- Uses DirectX 8 wrapper for surface operations
- Depends on WW3D window system for GDI operations
