# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/RGB.H

## Purpose
Defines the RGBClass for color representation and manipulation in the game engine.

## Responsibilities
- Encapsulates RGB color values (red, green, blue)
- Provides color conversion and comparison operations
- Supports color adjustment and difference calculation
- Maintains device-independent color representation (0-255 scale)

## Key Types
- **RGBClass (Class)**: Represents a color with red, green, and blue components.
- **BlackColor (RGBClass)**: Global constant for black color.

## Key Functions
### `Adjust(int ratio, RGBClass const & rgb)`
- Purpose: Adjusts the current color based on a ratio and another color.
- Calls: None visible.

### `Difference(RGBClass const & rgb) const`
- Purpose: Calculates the difference between two colors.
- Calls: None visible.

## Globals
- **BlackColor (RGBClass const)**: Predefined black color (0, 0, 0).

## Dependencies
- **PaletteClass**: Forward-declared, used as a friend class.
- **HSVClass**: Forward-declared, used for color conversion.
