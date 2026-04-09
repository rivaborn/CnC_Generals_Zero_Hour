# Generals/Code/Libraries/Source/WWVegas/WW3D2/render2d.cpp

## Purpose
Handles 2D rendering operations including quads, lines, text, and UI elements in the SAGE engine.

## Responsibilities
- Manages 2D geometry (vertices, UVs, colors, indices)
- Handles coordinate transformations and screen biasing
- Implements text rendering with fonts and clipping
- Configures shaders and render states for 2D primitives
- Supports various blend modes (alpha, additive, grayscale)

## Key Types
- **Render2DClass**: Base class for 2D rendering with texture, shader, and coordinate management
- **Render2DTextClass**: Extends Render2DClass for text rendering with fonts and wrapping
- **ShaderClass**: Handles shader configuration (blending, texturing, fog)
- **RectClass**: Used for screen coordinates and UV ranges
- **Vector2**: 2D coordinate structure

## Key Functions
### `Render2DClass::Render()`
- Purpose: Renders all accumulated 2D geometry
- Calls: `DX8Wrapper::Set_Viewport`, `DX8Wrapper::Set_Texture`, `DX8Wrapper::Set_Shader`, `DX8Wrapper::Draw_Triangles`

### `Render2DClass::Add_Quad()`
- Purpose: Adds a textured quad with vertex colors
- Calls: `Internal_Add_Quad_Indicies`, `Internal_Add_Quad_Vertices`, `Internal_Add_Quad_UVs`, `Internal_Add_Quad_Colors`

### `Render2DTextClass::Draw_Text()`
- Purpose: Renders text with font and color
- Calls: `Draw_Char`, `Get_Text_Extents`

### `Render2DClass::Convert_Vert()`
- Purpose: Converts screen coordinates to normalized device coordinates
- Calls: None (direct math operations)

## Globals
- **ScreenResolution (RectClass)**: Stores current screen dimensions

## Dependencies
- `render2d.h`, `mutex.h`, `ww3d.h`, `refcount.h`, `font3d.h`, `rect.h`, `texture.h`
- `matrix4.h`, `matrix3d.h`, `dx8wrapper.h`, `dx8indexbuffer.h`, `dx8vertexbuffer.h`
- `sortingrenderer.h`, `vertmaterial.h`, `dx8fvf.h`, `dx8caps.h`, `wwprofile.h`, `wwmemlog.h`, `assetmgr.h`
