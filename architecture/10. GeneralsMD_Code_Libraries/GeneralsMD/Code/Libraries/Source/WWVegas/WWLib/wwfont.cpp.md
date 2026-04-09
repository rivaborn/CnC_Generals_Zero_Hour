# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/wwfont.cpp

## Purpose
Implements the `WWFontClass` for rendering text in the SAGE engine, handling font metrics, spacing, and surface drawing.

## Responsibilities
- Font construction and data management
- Character and string width calculations
- Text rendering with clipping and color conversion
- Spacing and outline/shadow adjustments

## Key Types
- `WWFontClass` (Class): Font rendering and management
- `FontType` (Struct): Font data structure (external)
- `ConvertClass` (Class): Color conversion (external)
- `Surface` (Class): Render target (external)
- `Rect`, `Point2D` (Structs): Geometry primitives (external)

## Key Functions
### `WWFontClass::Print`
- Purpose: Renders text to a surface with clipping and color conversion
- Calls: `surface.Lock()`, `surface.Fill_Rect()`, `surface.Unlock()`, `converter->Convert_Pixel()`

### `WWFontClass::Char_Pixel_Width`
- Purpose: Returns pixel width of a character including X spacing
- Calls: None

### `WWFontClass::String_Pixel_Width`
- Purpose: Calculates total pixel width of a string
- Calls: `Char_Pixel_Width()`

### `WWFontClass::Set_XSpacing`
- Purpose: Sets horizontal spacing override for font
- Calls: `Get_Width()`

### `WWFontClass::Set_YSpacing`
- Purpose: Sets vertical spacing override for font
- Calls: `Get_Height()`

## Globals
- `fontpalette` (array): Default 16-color palette for font rendering

## Dependencies
- `wwfont.h`, `always.h`, `_convert.h`
- `Surface`, `Rect`, `Point2D`, `ConvertClass` (external)
- `MAX()` macro (external)
