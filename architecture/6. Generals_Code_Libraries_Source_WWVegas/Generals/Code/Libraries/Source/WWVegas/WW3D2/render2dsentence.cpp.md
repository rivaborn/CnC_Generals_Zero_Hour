# Generals/Code/Libraries/Source/WWVegas/WW3D2/render2dsentence.cpp

## Purpose
Handles 2D text rendering in the SAGE engine, managing fonts, text layout, and rendering operations.

## Responsibilities
- Manages font characters and their rendering
- Handles text layout and formatting (centering, wrapping)
- Builds and renders text as textures
- Supports additive blending and shader effects
- Maintains text positioning and clipping

## Key Types
- **Render2DSentenceClass**: Main class for 2D text rendering
- **FontCharsClass**: Font character management
- **FontCharsClassCharDataStruct**: Stores character rendering data
- **FontCharsBuffer**: Buffer for font character data

## Key Functions
### FindStartingXPos
- Purpose: Calculates starting X position for text rendering
- Calls: Not inferable from snippet

### Build_Sentence_Not_Centered
- Purpose: Builds text layout without centering
- Calls: Not inferable from snippet

### Get_Formatted_Text_Extents
- Purpose: Calculates dimensions of formatted text
- Calls: Build_Sentence_Not_Centered

## Globals
- **TEXTURE_OFFSET** (const int): Texture offset constant
- **no_TEST_PLACEMENT** (const int): Debug placement flag

## Dependencies
- render2dsentence.h
- surfaceclass.h
- texture.h
- wwprofile.h
- wwmemlog.h
- dx8wrapper.h
- ShaderClass, Vector2, WW3D, W3DNEW, REF_PTR_SET/RELEASE macros
