# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/hsv.h

## Purpose
Defines the HSVClass for hue-saturation-value color representation and manipulation.

## Responsibilities
- Encapsulate HSV color values (hue, saturation, value)
- Provide conversion to RGB
- Offer color adjustment and difference calculation
- Manage color value ranges (0-255)

## Key Types
- **HSVClass (Class)**: Represents a color in HSV space with hue, saturation, and value components.
- **RGBClass (Class)**: Forward-declared RGB color class (defined elsewhere).
- **(anonymous enum) (Enum)**: Contains MAX_VALUE constant (255).

## Key Functions
### HSVClass::Adjust
- Purpose: Adjusts HSV values based on a ratio and another HSV color.
- Calls: Not inferable.

### HSVClass::Difference
- Purpose: Computes the difference between two HSV colors.
- Calls: Not inferable.

### HSVClass::operator RGBClass
- Purpose: Converts HSV to RGB.
- Calls: Not inferable.

## Globals
- **BlackColor (HSVClass const)**: Static black color instance.

## Dependencies
- Forward-declares `RGBClass` (conversion target).
- No external symbols used.
