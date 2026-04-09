# Generals/Code/Tools/WW3D/pluglib/hsv.h

## Purpose
Defines the HSVClass for hue-saturation-value color representation and manipulation.

## Responsibilities
- Encapsulates HSV color data (hue, saturation, value)
- Provides conversion to RGB (forward declaration)
- Offers color adjustment and difference calculation
- Manages color value ranges (0-255)

## Key Types
- HSVClass (Class): Represents a color in HSV space with adjustment/difference operations
- RGBClass (Class): Forward-declared RGB color class (conversion target)
- (anonymous enum) (Enum): Contains MAX_VALUE constant (255)

## Key Functions
### HSVClass::Adjust
- Purpose: Adjusts HSV values based on a ratio and another HSV color
- Calls: Not inferable

### HSVClass::Difference
- Purpose: Computes the difference between two HSV colors
- Calls: Not inferable

### HSVClass::operator RGBClass
- Purpose: Converts HSV to RGB color representation
- Calls: Not inferable

## Globals
- BlackColor (HSVClass const): Static black color instance

## Dependencies
- Key includes: None visible
- External symbols: RGBClass (forward-declared)
