# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/render2d.h

## Purpose
Header file defining 2D rendering classes for the SAGE engine, including primitive drawing and text rendering.

## Responsibilities
- Declares `Render2DClass` for 2D primitives (quads, lines, outlines, gradients)
- Declares `Render2DTextClass` for text rendering with fonts
- Provides color conversion macros and screen resolution management
- Defines vertex, UV, and color handling for 2D rendering

## Key Types
- **Render2DClass (Class)**: 2D rendering primitive manager (quads, lines, outlines, gradients)
- **Render2DTextClass (Class)**: Text rendering with font support and clipping
- **Font3DInstanceClass (Class)**: Font instance (forward declared)
- **TextureClass (Class)**: Texture reference (forward declared)
- **Vector3 (Class)**: 3D vector (forward declared)
- **Vector4 (Class)**: 4D vector (forward declared)

## Key Functions
### `Add_Quad`
- Purpose: Adds a textured quad with optional color
- Calls: `Internal_Add_Quad_Vertices`, `Internal_Add_Quad_UVs`, `Internal_Add_Quad_Colors`, `Internal_Add_Quad_Indicies`

### `Add_Line`
- Purpose: Adds a line segment with width and color
- Calls: None (direct vertex/color/UV manipulation)

### `Draw_Text`
- Purpose: Renders text using the current font
- Calls: `Draw_Char` (for each character)

### `Set_Screen_Resolution`
- Purpose: Sets the screen resolution for coordinate scaling
- Calls: None

## Globals
- **ScreenResolution (RectClass)**: Static screen resolution storage

## Dependencies
- `vector.h`, `vector2.h`, `shader.h`, `widestring.h`, `rect.h`, `bittype.h`
- `W3DMPO` (base class for memory management)
- `DynamicVectorClass` (for vertex/UV/color storage)
