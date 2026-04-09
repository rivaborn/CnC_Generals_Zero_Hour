# Generals/Code/Libraries/Source/WWVegas/WW3D2/render2dsentence.h

## Purpose
Header file defining classes for rendering 2D text sentences in the SAGE engine.

## Responsibilities
- Declares `FontCharsClass` for font character rendering
- Declares `Render2DSentenceClass` for text sentence rendering
- Defines data structures for text rendering (surfaces, shaders, clipping)
- Provides interfaces for font management and text layout

## Key Types
- **FontCharsClass (Class)**: Manages font characters and GDI font rendering
- **Render2DSentenceClass (Class)**: Handles text sentence rendering with wrapping, clipping, and shaders
- **SentenceDataStruct (Struct)**: Stores surface and rectangle data for rendered text chunks
- **PendingSurfaceStruct (Struct)**: Tracks surfaces awaiting rendering
- **RendererDataStruct (Struct)**: Associates renderers with surfaces
- **FontCharsClassCharDataStruct (Class)**: Stores per-character rendering data
- **FontCharsBuffer (Class)**: Buffer for character data storage

## Key Functions
### `Build_Sentence`
- Purpose: Constructs a text sentence from input text
- Calls: `Build_Sentence_Centered`, `Build_Sentence_Not_Centered`

### `Draw_Sentence`
- Purpose: Renders the constructed sentence
- Calls: `Render2DClass` methods (not visible in header)

### `Build_Textures`
- Purpose: Creates textures for rendered text
- Calls: `Allocate_New_Surface`

### `Allocate_New_Surface`
- Purpose: Allocates a new surface for text rendering
- Calls: Not visible in header

## Globals
- **CHAR_BUFFER_LEN (Enum)**: Defines buffer size constant (32768)

## Dependencies
- `render2d.h`, `refcount.h`, `vector.h`, `vector2i.h`, `wwstring.h`, `win.h`
- `SurfaceClass`, `TextureClass`, `ShaderClass`, `Render2DClass` (external)
- GDI handles (`HFONT`, `HBITMAP`, `HDC`)
