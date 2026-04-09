# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/render2d.cpp

## Purpose
Handles 2D rendering operations in the SAGE engine, including text rendering, quads, lines, and outlines.

## Responsibilities
- Manages 2D geometry (vertices, UVs, colors, indices)
- Handles coordinate transformations and screen resolution
- Supports text rendering with fonts and clipping
- Configures rendering states (shaders, blending modes)
- Provides utility functions for common 2D primitives

## Key Types
- **Render2DClass**: Core 2D rendering class managing geometry and rendering
- **Render2DTextClass**: Extends Render2DClass for text rendering
- **ShaderClass**: Handles shader configuration (blending, texturing, etc.)

## Key Functions
### `Render2DClass::Render()`
- Purpose: Renders all accumulated 2D geometry
- Calls: `DX8Wrapper::Set_Viewport`, `DX8Wrapper::Set_Texture`, `DX8Wrapper::Draw_Triangles`

### `Render2DTextClass::Draw_Text()`
- Purpose: Renders text using a specified font
- Calls: `Draw_Char()`, `Font->Char_Spacing()`, `Font->Char_Height()`

### `Render2DClass::Add_Quad()`
- Purpose: Adds a textured quad to the render batch
- Calls: `Internal_Add_Quad_Indicies()`, `Internal_Add_Quad_Vertices()`

## Globals
- **ScreenResolution (RectClass)**: Stores current screen dimensions

## Dependencies
- `render2d.h`, `mutex.h`, `ww3d.h`, `refcount.h`, `font3d.h`, `texture.h`
- `matrix4.h`, `dx8wrapper.h`, `dx8indexbuffer.h`, `dx8vertexbuffer.h`
- `sortingrenderer.h`, `vertmaterial.h`, `dx8fvf.h`, `dx8caps.h`
