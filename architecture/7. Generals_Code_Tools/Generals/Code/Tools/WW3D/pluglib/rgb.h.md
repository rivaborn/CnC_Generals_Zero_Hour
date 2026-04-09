# Generals/Code/Tools/WW3D/pluglib/rgb.h

## Purpose
Defines a color representation class (RGBClass) and related utilities for the SAGE engine.

## Responsibilities
- Encapsulates RGB color values (0-255 per channel)
- Provides color manipulation methods (adjustment, difference calculation)
- Defines a global black color constant
- Supports conversion to HSV color space

## Key Types
- **RGBClass (Class)**: Represents a color with red, green, and blue components.
- **PaletteClass (Class)**: Forward-declared; likely manages color palettes.
- **HSVClass (Class)**: Forward-declared; represents HSV color space.
- **(anonymous enum)**: Contains MAX_VALUE=255 constant.

## Key Functions
### RGBClass::Adjust
- Purpose: Adjusts color values based on a ratio and another RGB color.
- Calls: None visible.

### RGBClass::Difference
- Purpose: Computes the difference between two RGB colors.
- Calls: None visible.

### RGBClass::operator=
- Purpose: Assigns one RGB color to another.
- Calls: None visible.

## Globals
- **BlackColor (RGBClass const)**: Represents the color black (0,0,0).

## Dependencies
- None (header-only, no external includes).
