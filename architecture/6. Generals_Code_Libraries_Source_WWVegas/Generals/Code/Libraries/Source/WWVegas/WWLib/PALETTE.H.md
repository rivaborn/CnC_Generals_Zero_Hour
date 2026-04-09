# Generals/Code/Libraries/Source/WWVegas/WWLib/PALETTE.H

## Purpose
Defines the `PaletteClass` for manipulating 256-color palettes in the game.

## Responsibilities
- Encapsulates a 256-color palette as an array of `RGBClass` objects.
- Provides operators and methods for palette manipulation (adjustment, comparison, color lookup).
- Supports conversion to/from raw binary palette data.

## Key Types
- **PaletteClass (class)**: Manages a 256-color palette with adjustment and lookup capabilities.

## Key Functions
### `Adjust(int ratio)`
- Purpose: Adjusts the brightness of the palette by a given ratio.
- Calls: Not inferable.

### `Adjust(int ratio, PaletteClass const & palette)`
- Purpose: Adjusts the palette relative to another palette using a ratio.
- Calls: Not inferable.

### `Partial_Adjust(int ratio, char *lut)`
- Purpose: Partially adjusts the palette using a lookup table.
- Calls: Not inferable.

### `Partial_Adjust(int ratio, PaletteClass const & palette, char *lut)`
- Purpose: Partially adjusts the palette relative to another palette using a lookup table.
- Calls: Not inferable.

### `Closest_Color(RGBClass const & rgb) const`
- Purpose: Finds the closest color index in the palette for a given RGB value.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `rgb.h` (for `RGBClass`)
