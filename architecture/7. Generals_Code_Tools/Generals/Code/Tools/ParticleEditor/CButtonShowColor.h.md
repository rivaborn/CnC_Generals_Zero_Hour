# Generals/Code/Tools/ParticleEditor/CButtonShowColor.h

## Purpose
Header for a custom button class that displays a color.

## Responsibilities
- Extends `CButton` to show a color visually
- Provides methods to get/set the displayed color
- Converts between RGB and BGR color formats
- Handles painting the color on the button

## Key Types
- CButtonShowColor (Class): Custom button that displays a color
- RGBColor (Type): Color data structure

## Key Functions
### getColor
- Purpose: Returns the current color.
- Calls: None

### setColor (Int)
- Purpose: Sets the color from an integer value.
- Calls: `m_color.setFromInt`

### setColor (RGBColor)
- Purpose: Sets the color from an RGBColor object.
- Calls: None

### RGBtoBGR
- Purpose: Converts RGB color to BGR format.
- Calls: None

### BGRtoRGB
- Purpose: Converts BGR color to RGB format.
- Calls: None

### OnPaint
- Purpose: Handles painting the color on the button.
- Calls: None

## Globals
- None

## Dependencies
- `CButton` (base class)
- `RGBColor` (color type)
- `COLORREF` (Windows color type)
- `DECLARE_MESSAGE_MAP()` (MFC
