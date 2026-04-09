# Generals/Code/Libraries/Source/WWVegas/WWLib/palette.cpp

## Purpose
Implements the PaletteClass for managing color palettes, including construction, comparison, assignment, and color adjustment operations.

## Responsibilities
- Construct and initialize palettes from RGB values or binary data
- Compare and assign palette objects
- Adjust palette colors toward black or another palette (with optional lookup table filtering)
- Find the closest color match in the palette

## Key Types
- **PaletteClass (Class)**: Manages a color palette with adjustment and comparison operations
- **RGBClass (Class)**: Used for color representation (referenced but not defined here)

## Key Functions
### PaletteClass::Adjust(int ratio)
- Purpose: Adjusts the palette toward black by a specified ratio
- Calls: Palette[index].Adjust(ratio, BlackColor)

### PaletteClass::Adjust(int ratio, PaletteClass const & palette)
- Purpose: Adjusts the palette toward another palette by a specified ratio
- Calls: Palette[index].Adjust(ratio, palette[index])

### PaletteClass::Partial_Adjust(int ratio, char *lut)
- Purpose: Adjusts specified palette entries toward black using a lookup table
- Calls: Palette[index].Adjust(ratio, BlackColor)

### PaletteClass::Partial_Adjust(int ratio, PaletteClass const & palette, char *lut)
- Purpose: Adjusts specified palette entries toward another palette using a lookup table
- Calls: Palette[index].Adjust(ratio, palette[index])

### PaletteClass::Closest_Color(RGBClass const & rgb) const
- Purpose: Finds the palette index of the color closest to the specified RGB value
- Calls: rgb.Difference(*ptr++)

## Globals
None

## Dependencies
- **Includes**: always.h, palette.h, string.h
- **External Types**: RGBClass, BlackColor
- **External Functions**: RGBClass::Adjust(), RGBClass::Difference(), memcpy, memcmp
