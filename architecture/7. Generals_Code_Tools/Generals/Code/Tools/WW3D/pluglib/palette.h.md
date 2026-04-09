# Generals/Code/Tools/WW3D/pluglib/palette.h

## Purpose
Defines the `PaletteClass` for manipulating 256-color palettes in the SAGE engine.

## Responsibilities
- Manages a 256-color palette as an array of `RGBClass` objects.
- Provides accessors and adjustment methods for palette colors.
- Supports palette comparison and conversion to raw byte arrays.

## Key Types
- **PaletteClass (Class)**: Wraps a 256-color palette with manipulation methods.
- **(anonymous enum) (Enum)**: Contains `COLOR_COUNT=256` constant.
- **COLOR_COUNT (Enum)**: Defines the number of colors in the palette (256).

## Key Functions
### `operator[]`
- Purpose: Access palette colors by index (with bounds checking).
- Calls: None.

### `Get_Color`
- Purpose: Returns a reference to a palette color by index.
- Calls: None.

### `operator==`
- Purpose: Compares two palettes for equality.
- Calls: None.

### `Adjust`
- Purpose: Adjusts palette colors by a given ratio.
- Calls: None.

### `Partial_Adjust`
- Purpose: Adjusts palette colors partially using a lookup table.
- Calls: None.

### `Closest_Color`
- Purpose: Finds the closest color in the palette to a given RGB value.
- Calls: None.

## Globals
- None.

## Dependencies
- `rgb.h` (for `RGBClass`).
