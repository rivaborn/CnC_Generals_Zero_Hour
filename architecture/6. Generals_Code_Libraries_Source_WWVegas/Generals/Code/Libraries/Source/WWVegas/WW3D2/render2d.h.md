# Generals/Code/Libraries/Source/WWVegas/WW3D2/render2d.h

## Purpose
Header file defining 2D rendering classes for the SAGE engine, including primitives, text, and shaders.

## Responsibilities
- Declares `Render2DClass` for 2D geometry rendering (quads, triangles, lines).
- Declares `Render2DTextClass` for 2D text rendering with fonts.
- Provides utility macros for color conversions (RGB/ARGB to/from INT32).
- Manages screen resolution and coordinate transformations.

## Key Types
- **Render2DClass (Class)**: 2D rendering interface for primitives and textures.
- **Render2DTextClass (Class)**: Extends `Render2DClass` for text rendering with fonts.
- **Font3DInstanceClass (Class)**: Forward declaration for font handling.
- **TextureClass (Class)**: Forward declaration for texture management.
- **Vector2 (Class)**: 2D vector math.
- **Vector3 (Class)**: 3D vector math (unused in this file).
- **Vector4 (Class)**: 4D vector math (unused in this file).
- **ShaderClass (Class)**: Shader management (included via header).

## Key Functions
### `Render2DClass::Add_Quad`
- Purpose: Adds a textured quad with optional color.
- Calls: `Internal_Add_Quad_Vertices`, `Internal_Add_Quad_UVs`, `Internal_Add_Quad_Colors`, `Internal_Add_Quad_Indicies`.

### `Render2DClass::Add_Line`
- Purpose: Adds a line segment with width and color.
- Calls: None directly (likely uses internal vertex/color methods).

### `Render2DTextClass::Draw_Text`
- Purpose: Renders text using the current font.
- Calls: `Draw_Char` for each character.

### `Render2DTextClass::Draw_Char`
- Purpose: Renders a single character.
- Calls: `Add_Quad` for glyph rendering.

## Globals
- **ScreenResolution (RectClass)**: Static member storing screen dimensions.

## Dependencies
- **Headers**: `always.h`, `simplevec.h`, `vector2.h`, `shader.h`, `widestring.h`, `rect.h`, `bittype.h`.
- **External Types**: `Font3DInstanceClass`, `TextureClass`, `Vector3`, `Vector4`, `ShaderClass`, `W3DMPO`, `SimpleDynVecClass`.
