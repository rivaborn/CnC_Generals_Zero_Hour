# Generals/Code/Tools/WW3D/pluglib/palette.cpp

## Purpose
Implements the PaletteClass for managing color palettes in the game engine.

## Responsibilities
- Constructs and initializes palettes
- Performs palette adjustments (fading, blending)
- Finds closest color matches in a palette
- Provides palette comparison and assignment operations

## Key Types
- PaletteClass (class): Manages a color palette with adjustment and comparison capabilities
- RGBClass (external): Represents a color (used but not defined here)

## Key Functions
### PaletteClass::Adjust(int ratio)
- Purpose: Adjusts palette toward black by specified ratio
- Calls: Palette[index].Adjust(ratio, BlackColor)

### PaletteClass::Adjust(int ratio, PaletteClass const & palette)
- Purpose: Adjusts palette toward another palette by specified ratio
- Calls: Palette[index].Adjust(ratio, palette[index])

### PaletteClass::Closest_Color(RGBClass const & rgb) const
- Purpose: Finds closest color match in palette
- Calls: rgb.Difference(*ptr++)

## Globals
None

## Dependencies
- "always.h"
- "palette.h"
- "string.h"
- RGBClass (external)
- BlackColor (external constant)
