# Generals/Code/Libraries/Source/WWVegas/WWLib/wwfont.cpp

## Purpose
Implements font rendering functionality for the SAGE engine, handling text display, measurement, and font metrics.

## Responsibilities
- Font construction and configuration
- Text rendering with clipping and spacing
- Font metric calculations (width/height)
- Character and string pixel width measurement

## Key Types
- `WWFontClass`: Font rendering class
- `FontType`: Font data structure (external)
- `ConvertClass`: Color conversion utility (external)
- `Surface`: Render target surface (external)

## Key Functions
### `WWFontClass::Print`
- Purpose: Renders text to a surface with clipping and formatting
- Calls: `surface.Lock()`, `surface.Fill_Rect()`, `surface.Unlock()`, `converter->Convert_Pixel()`

### `WWFontClass::Char_Pixel_Width`
- Purpose: Returns pixel width of a character including spacing
- Calls: None

### `WWFontClass::String_Pixel_Width`
- Purpose: Calculates total pixel width of a string
- Calls: `Char_Pixel_Width()`

### `WWFontClass::Set_XSpacing`
- Purpose: Sets horizontal character spacing override
- Calls: `Get_Width()`

### `WWFontClass::Set_YSpacing`
- Purpose: Sets vertical line spacing override
- Calls: `Get_Height()`

## Globals
- `fontpalette` (array): Default font color palette

## Dependencies
- `wwfont.h`, `always.h`, `_convert.h`
- `Surface`, `Point2D`, `Rect`, `ConvertClass` classes
- `MAX()` macro
