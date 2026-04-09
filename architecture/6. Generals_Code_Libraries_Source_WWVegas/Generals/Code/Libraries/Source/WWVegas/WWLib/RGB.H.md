# Generals/Code/Libraries/Source/WWVegas/WWLib/RGB.H

## Purpose
Defines the RGBClass for color representation and manipulation in the game engine.

## Responsibilities
- Encapsulates RGB color values (red, green, blue)
- Provides color manipulation methods (adjustment, difference calculation)
- Supports conversion to HSV color space
- Manages color value clamping (0-255 range)

## Key Types
- **RGBClass (Class)**: Represents a color with red, green, and blue components (0-255)
- **BlackColor (RGBClass)**: Global constant for black color

## Key Functions
### `Adjust(int ratio, RGBClass const & rgb)`
- Purpose: Adjusts the current color based on a ratio and another RGB color
- Calls: None visible

### `Difference(RGBClass const & rgb) const`
- Purpose: Calculates the difference between two RGB colors
- Calls: None visible

## Globals
- **BlackColor (RGBClass const)**: Predefined black color (0,0,0)

## Dependencies
- **PaletteClass**: Forward-declared, used as a friend class
- **HSVClass**: Forward-declared, used for conversion operator
