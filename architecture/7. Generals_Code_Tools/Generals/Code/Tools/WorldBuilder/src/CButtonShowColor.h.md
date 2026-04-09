# Generals/Code/Tools/WorldBuilder/src/CButtonShowColor.h

## Purpose
Header file defining a custom button class for displaying colors in the WorldBuilder tool.

## Responsibilities
- Extends `CButton` to show a color preview
- Provides color getters/setters
- Handles color format conversions (RGB/BGR)
- Manages painting behavior for color display

## Key Types
- **CButtonShowColor (Class)**: Custom button for color display with RGB/BGR conversion utilities
- **RGBColor (Type)**: Color representation used internally

## Key Functions
### `getColor`
- Purpose: Returns the current color.
- Calls: None

### `setColor` (Int)
- Purpose: Sets color from an integer value.
- Calls: `m_color.setFromInt`

### `setColor` (RGBColor)
- Purpose: Sets color from an RGBColor object.
- Calls: None

### `RGBtoBGR`
- Purpose: Converts RGB color to BGR format.
- Calls: None

### `BGRtoRGB`
- Purpose: Converts BGR color to RGB format.
- Calls: None

### `OnPaint`
- Purpose: Handles the button's painting to display the color.
- Calls: Not inferable

## Globals
- None

## Dependencies
- `CButton` (base class)
- `RGBColor` (external type
