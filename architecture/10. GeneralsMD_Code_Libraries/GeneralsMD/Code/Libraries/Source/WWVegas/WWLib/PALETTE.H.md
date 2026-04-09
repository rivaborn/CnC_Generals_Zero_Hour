# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/PALETTE.H

## Purpose
Defines the `PaletteClass` for manipulating 256-color palettes in the SAGE engine.

## Responsibilities
- Encapsulates palette data and operations
- Provides color access and manipulation methods
- Supports palette adjustments and comparisons
- Converts between RGB and palette formats

## Key Types
- **PaletteClass (class)**: Manages a 256-color palette with adjustment and lookup capabilities
- **COLOR_COUNT (enum)**: Constant for number of palette entries (256)

## Key Functions
### `operator[]`
- Purpose: Access palette color by index
- Calls: None

### `Adjust`
- Purpose: Adjust palette brightness/contrast
- Calls: None

### `Closest_Color`
- Purpose: Find nearest palette color for a given RGB value
- Calls: None

## Globals
- None

## Dependencies
- `rgb.h` (for `RGBClass`)
- Standard C++ types (`unsigned char`, `int`)
