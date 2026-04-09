# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/hsv.cpp

## Purpose
Implements HSV (Hue, Saturation, Value) color manipulation and conversion to RGB.

## Responsibilities
- Adjust HSV colors toward a target color with a specified ratio
- Calculate color differences between HSV objects
- Convert HSV colors to RGB format

## Key Types
- HSVClass: Represents an HSV color with hue, saturation, and value components
- RGBClass: External RGB color class (used in conversion operator)

## Key Functions
### HSVClass::Adjust
- Purpose: Adjusts the HSV color toward another HSV color by a specified ratio
- Calls: None

### HSVClass::Difference
- Purpose: Computes the difference between two HSV colors
- Calls: None

### HSVClass::operator RGBClass
- Purpose: Converts an HSV color to an RGB color
- Calls: None

## Globals
- HSVClass::BlackColor (HSVClass): Predefined black color constant

## Dependencies
- "always.h", "hsv.h", "rgb.h"
- RGBClass (external)
